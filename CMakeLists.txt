cmake_minimum_required(VERSION 3.5)
project(cypher)

include_directories(AFTER SYSTEM c:\\c++\\MinGW\\include)

set(TARGET cypher PROPERTY CXX_STANDARD 14)
set(TARGET cypher PROPERTY CXX_STANDARD_REQUIRED ON)

find_package(Boost 1.58.0 REQUIRED)

set(SOURCE_FILES main.cpp include/cypher/cypher.hpp include/cypher/hash/blake2b.hpp include/cypher/hash/md5.hpp include/cypher/hash/md5.cpp include/cypher/util/rotate_shift.hpp include/cypher/util/scrub.hpp)
add_executable(cypher ${SOURCE_FILES})