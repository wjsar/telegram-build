if(NOT DEFINED CMAKE_TOOLCHAIN_FILE)
    set(CMAKE_TOOLCHAIN_FILE "${CMAKE_CURRENT_SOURCE_DIR}/vcpkg/scripts/buildsystems/vcpkg.cmake"
        CACHE STRING "Vcpkg toolchain file")
endif()

# 添加 vcpkg 依赖
find_package(Qt5 COMPONENTS Core Gui Widgets Network REQUIRED)
find_package(OpenSSL REQUIRED)
find_package(ZLIB REQUIRED) 