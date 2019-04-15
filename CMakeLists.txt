cmake_minimum_required (VERSION 3.1)
project(teste_cgal)
find_package(CGAL)
add_executable(teste teste.cpp)
target_link_libraries(teste CGAL::CGAL)


# #CGAL_Qt5 is needed for the drawing and CGAL_Core is needed for this special Kernel.
# find_package(CGAL REQUIRED COMPONENTS Qt5)
# if(CGAL_FOUND AND CGAL_Qt5_FOUND)
#   #required to use basic_viewer
#   add_definitions(-DCGAL_USE_BASIC_VIEWER -DQT_NO_KEYWORDS)
#   #create the executable of the application
#   add_executable(teste_ teste.cpp)
#   #link it with the required CGAL libraries
#   target_link_libraries(teste_ CGAL::CGAL CGAL::CGAL_Qt5 CGAL::CGAL_Core)
# else()
#   message("ERROR: this program requires CGAL and CGAL_Qt5 and will not be compiled.")
# endif()