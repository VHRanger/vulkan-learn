This is to learn MoltenVK on MacOS. Follows [this](https://vulkan-tutorial.com/Drawing_a_triangle/Setup/Base_code) tutorial.

# Dependencies

GLFW
`brew install glfw3 --HEAD`

GLM
`brew install glm`

Vulkan SDK at https://vulkan.lunarg.com/

# Compiling

From this folder:

```
clear && clang++ main.cpp -I/usr/local/include -I/Users/mranger/Documents/Projects/vulkansdk-macos-1.2.131.2/macOS/include -L/usr/local/lib -L/Users/mranger/Documents/Projects/vulkansdk-macos-1.2.131.2/macOS/lib -std=c++1z -stdlib=libc++ -lvulkan.1.2.131 -lvulkan.1 -lglfw.3.4 && ./a.out
```

Change the vulkan SDK folder name and library version names as needed. Main needed libraries are `vulkan.1.x.xxx`, `vulkan.1`, `glfw3.x`


**Compiling Shaders**

from the `shaders` folder

`/Users/mranger/Documents/Projects/vulkansdk-macos-1.2.131.2/macOS/bin/glslc shader.vert -o vert.spv`

`/Users/mranger/Documents/Projects/vulkansdk-macos-1.2.131.2/macOS/bin/glslc shader.frag -o frag.spv`