cmake_minimum_required(VERSION 3.10)
project(lab04 VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
    set(CMAKE_INSTALL_PREFIX "${CMAKE_BINARY_DIR}/_install" CACHE PATH "..." FORCE)
endif()

file(GLOB SOURCES "src/*.cpp")
file(GLOB HEADERS "include/*.h")

if(NOT SOURCES)
    file(WRITE "${CMAKE_BINARY_DIR}/main.cpp"
        "#include <iostream>\n\nint main() {\n   std::cout << \"Hello from CI!\\n\";\n return 0;\n}\n")
    set(SOURCES "${CMAKE_BINARY_DIR}/main.cpp")
endif()

add_executable(${PROJECT_NAME} ${SOURCES})

if(HEADERS)
    install(FILES ${HEADERS} DESTINATION include)
endif()

install(TARGETS ${PROJECT_NAME} DESTINATION bin)

