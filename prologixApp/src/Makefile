TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = prologix
# prologix.dbd will be created and installed
DBD += prologix.dbd

# prologix.dbd will be made up from these files:
prologix_DBD += base.dbd

# Include dbd files from all support applications:
#prologix_DBD += xxx.dbd
prologix_DBD += calc.dbd
prologix_DBD += drvPrologixGPIB.dbd
prologix_DBD += stream.dbd
prologix_DBD += asyn.dbd
prologix_DBD += drvAsynSerialPort.dbd
# Add all the support libraries needed by this IOC
#prologix_LIBS += xxx
prologix_LIBS += calc
prologix_LIBS += drvPrologixGPIB
prologix_LIBS += stream
prologix_LIBS += asyn

# prologix_registerRecordDeviceDriver.cpp derives from prologix.dbd
prologix_SRCS += prologix_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
prologix_SRCS_DEFAULT += prologixMain.cpp
prologix_SRCS_vxWorks += -nil-

# Add support from base/src/vxWorks if needed
#prologix_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# Finally link to the EPICS Base libraries
prologix_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

