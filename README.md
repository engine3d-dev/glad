### Glad
* Adding cmake support for glad

### How to add CMake to your project
1.) Do `sudo make install`
2.) Then add the following lines in your cmake project file.
`find_package(glad REQUIRED)` 
`target_link_libraries(${PROJECT_NAME} glad::glad)`
