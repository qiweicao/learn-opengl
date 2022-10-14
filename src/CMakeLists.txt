message("main ${MAIN_INCLUDE}")
add_executable(main main.cpp)

# set(MAIN_INCLUDE ${PROJECT_SOURCE_DIR}/include)
# set(MAIN_LIBRARY ${PROJECT_SOURCE_DIR}/lib)

target_include_directories(
  main PUBLIC ${MAIN_INCLUDE}
)

target_link_libraries(
  main PUBLIC ${MAIN_LIBRARY}
)