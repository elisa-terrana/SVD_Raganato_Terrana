cmake_minimum_required(VERSION 3.12.0)
project(ParametricDiffusion LANGUAGES CXX C)

# https://eigen.tuxfamily.org/dox/TopicCMakeGuide.html
# find_package(Eigen3 3.3 REQUIRED NO_MODULE)

include(../common/cmake-common.cmake)

# add_executable(ParametricDiffusion src/ParametricDiffusion.cpp src/POD.cpp src/Poisson2D.cpp)
# deal_ii_setup_target(ParametricDiffusion)
# target_link_libraries (ParametricDiffusion Eigen3::Eigen)

# add_executable(ParametricDiffusion1D src/ParametricDiffusion1D.cpp src/POD.cpp src/Diffusion1D.cpp)
# deal_ii_setup_target(ParametricDiffusion1D)

add_executable(ParametricDiffusion1D_B src/ParametricDiffusion1D.cpp src/POD.cpp src/AdvDiff1D.cpp src/AdvDiff1D_POD.cpp)
deal_ii_setup_target(ParametricDiffusion1D_B)

# target_link_libraries (ParametricDiffusion1D Eigen3::Eigen)