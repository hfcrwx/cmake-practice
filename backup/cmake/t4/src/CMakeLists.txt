add_executable(main main.c)
# include_directories(/usr/include/hello)
find_path(myHeader hello.h)
if(myHeader)
	include_directories(${myHeader})
endif(myHeader)

# target_link_libraries(main hello)
target_link_libraries(main libhello.a)
