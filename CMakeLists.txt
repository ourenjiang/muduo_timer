cmake_minimum_required(VERSION 2.6)

project(muduo_timer)

set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR}/lib)

include_directories($ENV{HOME}/devtool/boost-1.84.0/include)

add_library(muduo_timer
Timestamp.cc
Channel.cc
CurrentThread.cc
EventLoop.cc
EPollPoller.cc
PollPoller.cc
Poller.cc
DefaultPoller.cc
SocketsOps.cc
Timer.cc
TimerQueue.cc
Timestamp.cc
Thread.cc
CountDownLatch.cc
Exception.cc
)

add_executable(main
main.cpp
)

target_link_libraries(main
muduo_timer
)
