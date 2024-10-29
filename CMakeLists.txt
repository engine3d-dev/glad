cmake_minimum_required(VERSION 3.15)

set(PROJECT_NAME glad)
project(${PROJECT_NAME} VERSION 1.0)
set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(CMAKE_CXX_VISIBILITY_PRESET hidden)
set(CMAKE_VISIBILITY_INLINES_HIDDEN ON)

option(GLAD_BUILD_UNIT_TESTS "Build the glad unit tests" ON)
option(GLAD_BUILD_TESTBED "Build the glad testbed" ON)
option(GLAD_BUILD_DOCS "Build the glad documentation" OFF)
option(GLAD_USER_SETTINGS "Override glad settings with gladUserSettings.h" OFF)

option(BUILD_SHARED_LIBS "Build Box2D as a shared library" OFF)

include(GNUInstallDirs)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

add_subdirectory(src)

install(
  DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/include/glad"
  DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
)