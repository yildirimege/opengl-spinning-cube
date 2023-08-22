set(SOURCES
    main.cpp
    cube_renderer.cpp
)

set(HEADERS
    include/cube_renderer.h
)

# Find required packages
find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

# Add an executable target
add_executable(OpenGLCube
    ${SOURCES}
    ${HEADERS})

# Link libraries
target_link_libraries(OpenGLCube PRIVATE OpenGL::GL glfw)

# Set C++ standard and compile options
target_compile_features(OpenGLCube PRIVATE cxx_std_11)
