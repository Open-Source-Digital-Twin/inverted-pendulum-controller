enable_testing()

include_directories(mocks)

add_subdirectory(config)
add_subdirectory(controller)
add_subdirectory(hal)

add_executable(
  hello_test
  hello_test.cpp
)

target_link_libraries(
  hello_test
  GTest::gtest_main
)

include(GoogleTest)
gtest_discover_tests(hello_test)
