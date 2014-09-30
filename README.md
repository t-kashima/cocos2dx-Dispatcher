cocos2dx-Dispatcher
===================

Cocos2d-xで簡単に別スレッドを立てたり、メインスレッドを呼び出すためのクラスです。

```C++

std::cout << "thread is: " << std::this_thread::get_id() << std::endl;

// new thread
Dispatcher::execBackground([=] {

  std::cout << "thread is: " << std::this_thread::get_id() << std::endl;
  
  // main thread
  Dispatcher::execMain([=] {
    std::cout << "thread is: " << std::this_thread::get_id() << std::endl;
  });
});
```
