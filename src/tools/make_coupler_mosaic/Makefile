# The following three directory may need to set.
include $(PWD)/../../../mkmf/configure.mkmf

OBJS = mosaic_util.o create_xgrid.o mpp.o mpp_domain.o mpp_io.o make_coupler_mosaic.o tool_util.o interp.o

HEADERS = Makefile $(TOOLSHAREDIR)/mpp.h  $(TOOLSHAREDIR)/mpp_domain.h   \
          $(TOOLSHAREDIR)/mpp_io.h $(SHAREDIR)/mosaic_util.h                    \
          $(SHAREDIR)/create_xgrid.h
make_coupler_mosaic: $(OBJS)
	$(CC) $(LNFLAGS) -o $@ $(OBJS) $(LDFLAGS)

make_coupler_mosaic.o: $(COREDIR)/make_coupler_mosaic.c $(HEADERS)
	$(CC) $(CFLAGS) -c $(COREDIR)/make_coupler_mosaic.c 

mosaic_util.o: $(SHAREDIR)/mosaic_util.c $(HEADERS)
	$(CC) $(CFLAGS) -c $(SHAREDIR)/mosaic_util.c

create_xgrid.o: $(SHAREDIR)/create_xgrid.c $(HEADERS)
	$(CC) $(CFLAGS) -c $(SHAREDIR)/create_xgrid.c 

mpp.o: $(TOOLSHAREDIR)/mpp.c $(HEADERS)
	$(CC) $(CFLAGS) -c $(TOOLSHAREDIR)/mpp.c 

mpp_domain.o: $(TOOLSHAREDIR)/mpp_domain.c $(HEADERS)
	$(CC) $(CFLAGS) -c $(TOOLSHAREDIR)/mpp_domain.c 

mpp_io.o: $(TOOLSHAREDIR)/mpp_io.c $(HEADERS)
	$(CC) $(CFLAGS) -c $(TOOLSHAREDIR)/mpp_io.c

interp.o: $(SHAREDIR)/interp.c $(HEADERS)
	$(CC) $(CFLAGS) -c $(SHAREDIR)/interp.c 

tool_util.o: $(TOOLSHAREDIR)/tool_util.c $(HEADERS)
	$(CC) $(CFLAGS) -c $(TOOLSHAREDIR)/tool_util.c
