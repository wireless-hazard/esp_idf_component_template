# Template for esp idf component

Put all your source files (.c and .cpp) into the folder **src/** and all of your header files (.h or .hpp) into the **include/** folder

After that, you only have to list all your source files in the **CMakeLists.txt**

Ex:
```cmake
set(COMPONENT_SRCS
    "src/modbus_slave.cpp"
    "src/modbus_master.cpp"
    "src/modbus_utils.cpp")
```
and then you have to give your library's folder name as the name registered in the **CMakeLists.txt** as well

Ex:

```cmake
register_component(modbus_important_library)
```
## Examples folder

You can use this own component to test your code without including it into another project. To do that, put your example code into examples/main/app_main.cpp

If your project has another dependency beyond the library you're implementing, add the corresponding folder into **examples/CMakeLists.txt**

Ex:
```cmake
set(EXTRA_COMPONENT_DIRS ${PWD}../../modbus_important_library
                         ${PWD}../../outside_dependency)
```
