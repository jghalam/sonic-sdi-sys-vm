data_sdidir= $(sysconfdir)/sonic/sdi
data_sdi_DATA = cfg/sdi/*.sql 
bin_SCRIPTS = cfg/sdi/platform_init.sh

#The sdi-sys library
lib_LTLIBRARIES = libsonic_sdi_db.la

libsonic_sdi_db_la_SOURCES = src/sdi_db_ops.c
libsonic_sdi_db_la_LDFLAGS = -lsonic_db_sql -version-info 1:1:0
libsonic_sdi_db_la_CFLAGS = -I$(top_srcdir)/sonic  -I$(includedir)/sonic  -I$(top_srcdir)/sonic/private

lib_LTLIBRARIES += libsonic_sdi_sys.la

libsonic_sdi_sys_la_SOURCES =  src/sdi_vm_entity.c \
                src/sdi_vm_media.c \
                src/sdi_vm_sys.c \
                src/sdi_vm_fan.c \
                src/sdi_vm_led.c \
                src/sdi_vm_thermal.c


libsonic_sdi_sys_la_LDFLAGS = -lsonic_sdi_db -lsonic_db_sql -lsonic_logging -lpthread -lrt -version-info 1:1:0
libsonic_sdi_sys_la_CFLAGS = -I$(top_srcdir)/sonic  -I$(includedir)/sonic  -I$(top_srcdir)/sonic/private





