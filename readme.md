# #TLS(线程局部存储）

1. int     pthread_once(pthread_once_t *once_control, void (*init_routine) (void))；

   本函数使用初值为PTHREAD_ONCE_INIT的once_control变量保证init_routine()函数在本进程执行序列中仅执行一次。  

​    2. int  pthread_key_create(pthread_key_t *key, void (*destr_function) (void *))      该函数从TSD池中分配一项，将其值赋给key供以后访问使用。如果destr_function不为空，在线程退出（pthread_exit()）时将以key所关联的数据为参数调用destr_function()，以释放分配的缓冲区。        

 

3.pthread_getpecific和pthread_setspecific提供了在同一个线程中不同函数间共享数据即线程存储的一种方法

4.pthread_getpecific     会在本线程中找key值得实例

5.pthread_setspecific会将key值和实例进行绑定



