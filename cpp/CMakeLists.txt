project (miniball CXX)
cmake_minimum_required (VERSION 2.8.11)

include_directories (main)

add_executable (test_fromfile
   test/fromfile.cpp
   )

enable_testing ()

SET (testdir ${CMAKE_CURRENT_SOURCE_DIR}/test)

add_test (working_1 test_fromfile ${testdir}/test_working_1.txt)
add_test (infinite_loop_1 test_fromfile ${testdir}/test_infinite_loop_1.txt)
add_test (infinite_loop_2 test_fromfile ${testdir}/test_infinite_loop_2.txt)
add_test (infinite_loop_3 test_fromfile ${testdir}/test_infinite_loop_3.txt)
