cmake_minimum_required(VERSION 2.8.3)
project(quadSYSspline)
LIST( APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake )
find_package(Eigen3 REQUIRED)
find_package(Boost REQUIRED COMPONENTS system filesystem)

# enable dashboard scripting
include (CTest)
set (CTEST_PROJECT_NAME "quadSYSspline")

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
#find_package(catkin REQUIRED COMPONENTS)

###########
## Build ##
###########
include_directories( ${PROJECT_SOURCE_DIR}/include )
include_directories( ${Boost_INCLUDE_DIRS} )
include_directories( ${EIGEN3_INCLUDE_DIRS} )

add_executable(quadSYSspline src/quadSYSspline.cpp)
TARGET_LINK_LIBRARIES( quadSYSspline ${Boost_LIBRARIES} )
#target_link_libraries(actor_critic_lib function_approximation_lib)
#target_link_libraries(CartPoleBalancing actor_critic_lib)

#############
## Install ##
#############

# To Do

#############
## Testing ##
#############

# To Do
