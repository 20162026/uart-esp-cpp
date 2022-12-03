cmake_minimum_required(VERSION 3.5)

set(srcs "pl_uart_base.cpp" "pl_uart_server.cpp" )
add_prefix(srcs "${CMAKE_CURRENT_LIST_DIR}/" ${srcs})

idf_component_register( SRCS ${srcs} 
                        INCLUDE_DIRS "include" 
                        REQUIRES driver pl_common)

target_compile_options(${COMPONENT_LIB} PRIVATE -frtti)