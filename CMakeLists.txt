cmake_minimum_required(VERSION 3.1)

project(OrganicDumpClient VERSION 1.0)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/build/cmake/find-modules")

add_subdirectory(external/googletest/repo/googletest)

set(GFLAGS_IS_SUBPROJECT TRUE)
set(GFLAGS_NAMESPACE "google")
#set(BUILD_SHARED_LIBS TRUE)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)
add_subdirectory(external/gflags/repo)
add_subdirectory(external/glog/repo)
#add_subdirectory(external/mysql-cpp/repo)

add_subdirectory(code/sentry-client/repo)
add_subdirectory(code/xbox-controller/repo)
add_subdirectory(code/gpio14/repo)
add_subdirectory(code/mysql-cpp-prebuilts/repo)
add_subdirectory(code/bluez-prebuilts/repo)
add_subdirectory(code/glib-prebuilts/repo)
add_subdirectory(code/dbus-prebuilts/repo)
add_subdirectory(external/boringssl/repo)
add_subdirectory(external/protobuf/repo/cmake)
add_subdirectory(external/jsoncpp/repo)
