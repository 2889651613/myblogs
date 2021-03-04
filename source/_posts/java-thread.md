---
  title: java-thread
---
### java线程是的实现方式

   1. 继承Thread 类

           class ThreadDemo extend Thread{
              public static void main(String[] args){
                ThreadDemo t=new ThreadDemo();
               t.start();
           }
       }

   2. 实现 Runnable 接口

           class RunnabelDemo implements Runnable{
              public static void main(String[] args){
                RunnableDemo r=new RunnableDemo();
                Thread t=new Thread(r);
                t.start(); 
          }
      }

   3. 实现callable 接口 和 Future

### 线程同异不同

### 线程锁

1. 同步锁

2. 异步锁

### 线程安全

### CAS以及ABA问题

### 线程池
