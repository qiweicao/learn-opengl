message("main ${MAIN_INCLUDE}")
add_executable(main main.cpp)


target_include_directories(
  main PUBLIC ${MAIN_INCLUDE}
)

target_link_libraries(
  main PUBLIC ${MAIN_LIBRARY}
)