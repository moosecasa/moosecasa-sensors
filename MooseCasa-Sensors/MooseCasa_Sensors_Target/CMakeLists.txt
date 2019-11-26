add_avr_executable(
   MooseCasa_Sensors
   main.c
)

# find_library(M_LIB m)
# message(STATUS "avr-libm: ${M_LIB}")

find_library(C_LIB c)
message(STATUS "avr-libc: ${C_LIB}")

avr_target_link_libraries(MooseCasa_Sensors libm ${C_LIB})