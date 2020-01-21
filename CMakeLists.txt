# Cmake in OpenVPN3 core is mainly used to get Clion editior support and to run unit tests. For normal
# Build instructions see the README.rst

cmake_policy(SET CMP0048 NEW)
project(OpenVPN3-core VERSION 3)

cmake_minimum_required(VERSION 3.5)

add_subdirectory(test/unittests)
add_subdirectory(test/ovpncli)

if (WIN32)
    add_subdirectory(openvpn/omi)
endif ()
