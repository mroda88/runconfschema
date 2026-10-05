cmake_minimum_required(VERSION 3.12)
project(runconfschema VERSION 0.0.0)

find_package(daq-cmake REQUIRED)

daq_setup_environment()

find_package(Protobuf REQUIRED)
# find_package(gRPC REQUIRED)

daq_protobuf_codegen( *.proto)

daq_add_library(*.cpp)

daq_install()