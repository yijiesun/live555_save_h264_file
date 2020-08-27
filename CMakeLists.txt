cmake_minimum_required(VERSION 2.8)

project(save_264)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES main.cpp)


include_directories(
        /usr/local/include/
        /usr/local/include/groupsock
        /usr/local/include/liveMedia
        /usr/local/include/BasicUsageEnvironment
        /usr/local/include/UsageEnvironment
        )     
add_executable(save_264 ${SOURCE_FILES})
target_link_libraries(save_264  pthread   avformat avcodec -lBasicUsageEnvironment -lUsageEnvironment -lliveMedia -lgroupsock)