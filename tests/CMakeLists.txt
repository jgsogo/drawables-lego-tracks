cmake_minimum_required(VERSION 3.15)

find_package(Catch2 REQUIRED)

enable_testing()

add_executable(unit_tests
        main.cpp

        # TODO: Add your 'test_xxxx.cpp' files here
        )
target_link_libraries(unit_tests
        Catch2::Catch2
        ${PROJECT_NAME}
        )

# Load and use the .cmake file provided by Catch so all the test cases
# are made available to CTest.
include(Catch)
catch_discover_tests(unit_tests)
