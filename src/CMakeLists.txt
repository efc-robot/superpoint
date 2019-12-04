set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/lib)
SET(SRC_LIST SuperPoint.cpp)
add_library(${PROJECT_NAME} SHARED ${SRC_LIST}) 

target_link_libraries(${PROJECT_NAME}
${OpenCV_LIBS}
${CAFFE_DIR}/build/lib/libcaffe.so
${GLOG_BOOST_LIBS}
)
