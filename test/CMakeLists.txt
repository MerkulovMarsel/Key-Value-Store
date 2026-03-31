include(FetchContent)

FetchContent_Declare(
        googletest
        URL https://github.com/google/googletest/archive/refs/tags/v1.14.0.zip
        DOWNLOAD_EXTRACT_TIMESTAMP TRUE
)
FetchContent_MakeAvailable(googletest)


add_executable(simple_test test.cpp)
target_link_libraries(simple_test PRIVATE config  dumbmap server GTest::gtest_main)

include(GoogleTest)
gtest_discover_tests(simple_test)