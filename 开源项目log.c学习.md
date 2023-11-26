### 1. log.c项目介绍
***
+ 项目地址： https://github.com/rxi/log.c
+ 项目介绍：一个使用C语言编写的日志库项目，主要功能是实现日志写入（分级），支持多线程写入
### 2. 项目基本设计

```
/* 日志数据结构设计 */
typedef struct {
  va_list ap;        //用于遍历可变参数
  const char *fmt;   //格式化数据
  const char *file;  //保存日志的文件
  struct tm *time;   //记录系统时间
  void *udata;       //日志打印内容
  int line;          //函数行数
  int level;         //日志等级
} log_Event;
``` 
* 基本函数介绍：
  log_set_quiet(bool enable) //设置true后将不会输出任何内容到stderr，但会正常写日志和触发回调函数

  log_set_level(int level)   //低于给定级别的日志将不会写入stderr（终端输出），默认级别为trace

  log_add_fp(FILE *fp, int level) //将不同的级别的日志写入新的文件内

  log_add_callback(log_LogFn fn, void *udata, int level) //设置回调函数

  log_set_lock(log_LockFn fn, void *udata) //多线程写入日志时，加锁

  log_level_string(int level) // 将日志等级返回为字符串

  LOG_USE_COLOR //编译时用户可以传入的参数，用于设置
  
* 管理结构体L的设计，以及==callback结构体的设计==
* va_list的使用、va_start. va_end  \_\_VA_ARGS\_\_(可变参数的个数)
* 