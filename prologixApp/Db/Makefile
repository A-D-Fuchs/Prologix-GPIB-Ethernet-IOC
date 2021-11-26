TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE

#----------------------------------------------------
# Create and install (or just install) into <top>/db
# databases, templates, substitutions like this
#DB += xxx.db
DB += gpib_win.db
DB += gpib_e5270.db
DB += e5270.proto
DB += gpib_34401.db
DB += 34401.proto
DB += gpib_b2912.db
DB += b2912.proto
DB += gpib_k220.db
DB += k220.proto
DB += devSCPI.proto
#DB_INSTALLS += $(TOP)/gpibApp/Db/devSCPI.proto
DB_INSTALLS += $(ASYN)/db/asynRecord.db

#----------------------------------------------------
# If <anyname>.db template is not named <anyname>*.template add
# <anyname>_template = <templatename>

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

