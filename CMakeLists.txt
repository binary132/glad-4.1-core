set(GLAD_SRCS src/glad.c)

add_library(GLAD SHARED ${GLAD_SRCS})

target_include_directories(GLAD PRIVATE ${CMAKE_CURRENT_LIST_DIR}/include)

target_link_libraries(GLAD ${CMAKE_DL_LIBS})

find_path(GLAD_INCLUDE_DIR
  "glad/glad.h"
  PATHS ${CMAKE_CURRENT_LIST_DIR}
  PATH_SUFFIXES "include"
)
