set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/example)

add_executable(example example.cpp)

target_link_libraries(example
${OpenCV_LIBS}
${CAFFE_DIR}/build/lib/libcaffe.so
${GLOG_BOOST_LIBS}
${PROJECT_SOURCE_DIR}/lib/libsuperpoint.so
)
