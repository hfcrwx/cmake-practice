cmake_minimum_required(VERSION 2.6)
project(HELLO C)
# add_subdirectory(src bin)
add_subdirectory(src)

install(FILES COPYRIGHT README DESTINATION share/doc/cmake/t2)
install(PROGRAMS runhello.sh DESTINATION bin)
install(DIRECTORY doc/ DESTINATION share/doc/cmake/t2)
