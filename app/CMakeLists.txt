cmake_minimum_required(VERSION 3.18)

# set(CMAKE_FIND_DEBUG_MODE TRUE)
# set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

project("app") # ${PROJECT_NAME}

find_package(CGAL 6.2 EXACT REQUIRED) # PATHS "P:\\Downloads\\cpp-libraries\\portaudio\\build\\cmake\\portaudio")

if(CGAL_FOUND)
    message(STATUS "YES")
else()
    message(STATUS "NO")
endif()

add_executable("app"
    "src/main.cpp"
)

target_link_libraries("app" CGAL)
target_link_options("app" PRIVATE "-static")


