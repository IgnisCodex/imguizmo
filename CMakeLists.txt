cmake_minimum_required(VERSION 3.10)
project(imguizmo)

set(CMAKE_CXX_STANDARD 17)

# Source files
set(SOURCES
    ImGuizmo.cpp
    ImGradient.cpp
    ImSequencer.cpp
    GraphEditor.cpp
    ImCurveEdit.cpp
)

# Header files (optional, for IDEs)
set(HEADERS
    ImGuizmo.h
    ImGradient.h
    ImSequencer.h
    GraphEditor.h
    ImCurveEdit.h
    ImZoomSlider.h
)

# Build static library
add_library(imguizmo STATIC ${SOURCES} ${HEADERS})

target_include_directories(imguizmo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(imguizmo PUBLIC imgui)