add_executable(shell-app main.cpp AnalogSensor.cpp)

include_directories(
    ${CMAKE_SOURCE_DIR}/include
)

TARGET_LINK_LIBRARIES(shell-app ${ITK_LIBRARIES})

