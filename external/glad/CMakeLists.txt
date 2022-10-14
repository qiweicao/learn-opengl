project(glad C)

# file(GLOB_RECURSE GLAD_HEADERS
#   ${CMAKE_CURRENT_SOURCE_DIR}/include/*.h
# )

set(SOURCE_FILES
  ${CMAKE_CURRENT_SOURCE_DIR}/include/glad/glad.h
  ${CMAKE_CURRENT_SOURCE_DIR}/include/KHR/khrplatform.h
  ${CMAKE_CURRENT_SOURCE_DIR}/src/glad.c
)

add_library(glad STATIC ${SOURCE_FILES})
target_include_directories(glad
          PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include
          )