add_library(imgui imgui.cpp imgui_demo.cpp imgui_draw.cpp imgui_tables.cpp imgui_widgets.cpp)
target_include_directories(imgui PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")

add_library(imgui-glfw backends/imgui_impl_glfw.cpp)
target_include_directories(imgui-glfw PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/backends")
target_link_libraries(imgui-glfw PUBLIC imgui glfw)

add_library(imgui-wgpu backends/imgui_impl_wgpu.cpp)
target_include_directories(imgui-wgpu PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/backends")
target_link_libraries(imgui-wgpu PUBLIC imgui webgpu)
