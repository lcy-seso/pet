cmake_minimum_required(VERSION 3.0)

project (pet_parser C)

set(TARGET_NAME pet_parser)

set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -Wall -g0")
set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} -Wall")

include_directories(/home/yincao/.local/include)

link_directories(/home/yincao/.local/lib)

set(SRCS main.c emit.c)

add_executable(${TARGET_NAME} ${SRCS})
target_link_libraries(${TARGET_NAME} -lpet -lisl -lyaml)
