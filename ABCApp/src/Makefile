TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = ABC
# ABC.dbd will be created and installed
DBD += ABC.dbd

# ABC.dbd will be made up from these files:
ABC_DBD += base.dbd

# Include dbd files from all support applications:
#ABC_DBD += xxx.dbd

# Add all the support libraries needed by this IOC
#ABC_LIBS += xxx

# ABC_registerRecordDeviceDriver.cpp derives from ABC.dbd
ABC_SRCS += ABC_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
ABC_SRCS_DEFAULT += ABCMain.cpp
ABC_SRCS_vxWorks += -nil-

# Add support from base/src/vxWorks if needed
#ABC_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# Finally link to the EPICS Base libraries
ABC_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

