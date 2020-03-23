cmake_minimum_required(VERSION 2.8.3)
project(temizlik_robotu)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  nav_msgs
  sensor_msgs
  geometry_msgs
  message_generation
)

 add_message_files(
   FILES
   MesafeBilgisi.msg
 )

add_service_files(
    FILES 
    BilgiServisi.srv
    EngelBilgi.srv
)

 generate_messages(
   DEPENDENCIES
   std_msgs
   nav_msgs
   sensor_msgs
   geometry_msgs
 )

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

foreach(dir launch msg srv params src)
    install(DIRECTORY ${dir}/
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach()
