# sudo apt-get install libcurl4-openssl-dev
add_executable(curltest main.c)

# target_link_libraries(curltest curl)

find_package(CURL)
if(CURL_FOUND)
	include_directories(${CURL_INCLUDE_DIR})
	target_link_libraries(curltest ${CURL_LIBRARY})
else()
	message(FATAL_ERROR "CURL library not found")
endif()
