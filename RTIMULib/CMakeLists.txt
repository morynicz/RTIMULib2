#////////////////////////////////////////////////////////////////////////////
#//
#//  This file is part of RTIMULib
#//
#//  Copyright (c) 2014-2015, richards-tech
#//
#//  Permission is hereby granted, free of charge, to any person obtaining a copy of
#//  this software and associated documentation files (the "Software"), to deal in
#//  the Software without restriction, including without limitation the rights to use,
#//  copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the
#//  Software, and to permit persons to whom the Software is furnished to do so,
#//  subject to the following conditions:
#//
#//  The above copyright notice and this permission notice shall be included in all
#//  copies or substantial portions of the Software.
#//
#//  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,
#//  INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
#//  PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
#//  HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
#//  OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
#//  SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

#// The cmake support was based on work by Moritz Fischer at ettus.com.
#// Original copyright notice:
#
# Copyright 2014 Ettus Research LLC
#

########################################################################
IF(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_BINARY_DIR})
    MESSAGE(FATAL_ERROR "Prevented in-tree built. This is bad practice.")
ENDIF(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_BINARY_DIR})

########################################################################
# Project setup
########################################################################
ENABLE_TESTING()

add_library(RTIMULib
    src/IMUDrivers/RTHumidity.cpp
    src/IMUDrivers/RTHumidityHTU21D.cpp
    src/IMUDrivers/RTIMUBNO055.cpp
    src/IMUDrivers/RTIMUGD20HM303D.cpp
    src/IMUDrivers/RTIMUGD20M303DLHC.cpp
    src/IMUDrivers/RTIMULSM9DS1.cpp
    src/IMUDrivers/RTIMUMPU9250.cpp
    src/IMUDrivers/RTIMUNull.cpp
    src/IMUDrivers/RTPressure.cpp
    src/IMUDrivers/RTPressureMS5611.cpp
    src/IMUDrivers/RTHumidityHTS221.cpp
    src/IMUDrivers/RTIMUBMX055.cpp
    src/IMUDrivers/RTIMU.cpp
    src/IMUDrivers/RTIMUGD20HM303DLHC.cpp
    src/IMUDrivers/RTIMULSM9DS0.cpp
    src/IMUDrivers/RTIMUMPU9150.cpp
    src/IMUDrivers/RTIMUMPU9255.cpp
    src/IMUDrivers/RTPressureBMP180.cpp
    src/IMUDrivers/RTPressureLPS25H.cpp
    src/IMUDrivers/RTPressureMS5637.cpp
    src/RTFusion.cpp
    src/RTFusionKalman4.cpp
    src/RTFusionRTQF.cpp
    src/RTIMUAccelCal.cpp
    src/RTIMUHal.cpp
    src/RTIMUMagCal.cpp
    src/RTIMUSettings.cpp
    src/RTMath.cpp)
target_include_directories(RTIMULib PUBLIC include)