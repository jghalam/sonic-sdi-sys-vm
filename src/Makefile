LIBRARIES=sdi_db sdi_sys_v2

UNIT_TEST=  sdi_vm_entity_info_unittest \
            sdi_vm_media_unittest \
            sdi_vm_thermal_unittest \
            sdi_vm_fan_unittest \
            sdi_vm_led_unittest

SUBDIRS=unit_test

# Files for libsdi_db
sdi_db_SRCS=sdi_db_ops.c

sdi_db_LDFLAGS=-ldb_sql

# Files for libsdi_sys_v2
sdi_sys_v2_SRCS=   sdi_vm_entity.c \
                sdi_vm_media.c \
                sdi_vm_sys.c \
                sdi_vm_fan.c \
                sdi_vm_led.c \
                sdi_vm_thermal.c

# Since libsdi_db hasn't yet been copied over to opt/ngos/lib, add the current
# location to the paths to be searched by the linker
sdi_sys_v2_LDFLAGS=-lsdi_db -ldb_sql -levent_log -L${BUILD_CURDIR_sos}

sdi_vm_thermal_unittest_SRCS=unit_test/sdi_vm_thermal_unittest.cpp
sdi_vm_thermal_unittest_LDFLAGS=-lsdi_sys_v2 -lsdi_db

sdi_vm_entity_info_unittest_SRCS=unit_test/sdi_vm_entity_info_unittest.cpp
sdi_vm_entity_info_unittest_LDFLAGS=-lsdi_sys_v2 -lsdi_db

sdi_vm_fan_unittest_SRCS=unit_test/sdi_vm_fan_unittest.cpp
sdi_vm_fan_unittest_LDFLAGS=-lsdi_sys_v2 -lsdi_db

sdi_vm_media_unittest_SRCS=unit_test/sdi_vm_media_unittest.cpp
sdi_vm_media_unittest_LDFLAGS=-lsdi_sys_v2 -lsdi_db

sdi_vm_led_unittest_SRCS=unit_test/sdi_vm_led_unittest.cpp
sdi_vm_led_unittest_LDFLAGS=-lsdi_sys_v2 -lsdi_db

include ${MAKE_INC}/workspace.mak
