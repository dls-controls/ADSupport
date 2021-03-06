TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================


ifeq ($(WITH_HDF5),YES)
  ifeq ($(HDF5_EXTERNAL),NO)

    LIBRARY_IOC = hdf5
    PROD_IOC    = H5detect

    USR_CFLAGS += -D NDEBUG
    ifeq ($(SHARED_LIBRARIES), YES)
      USR_CFLAGS_WIN32 += -D H5_BUILT_AS_DYNAMIC_LIB 
      USR_CFLAGS_WIN32 += -D hdf5_shared_EXPORTS
      ifeq (mingw, $(findstring mingw, $(T_A)))
        USR_CFLAGS_WIN32 += -D__MSVCRT_VERSION__=0x800
      else
        # The thread code on mingw needs work, get compiler errors
        USR_CFLAGS_WIN32 += -D H5_HAVE_THREADSAFE
      endif
    endif

    INC += H5ACpublic.h
    INC += H5api_adpt.h
    INC += H5Apublic.h
    INC += H5B2public.h
    INC += H5Bpublic.h
    INC += H5Cpublic.h
    INC += H5Dpublic.h
    INC += H5Epubgen.h
    INC += H5Epublic.h
    INC += H5FDcore.h
    INC += H5FDdirect.h
    INC += H5FDfamily.h
    INC += H5FDlog.h
    INC += H5FDmpi.h
    INC += H5FDmpio.h
    INC += H5FDmulti.h
    INC += H5FDpublic.h
    INC += H5FDsec2.h
    INC += H5FDstdio.h
    INC += H5FDwindows.h
    INC += H5FSpublic.h
    INC += H5Fpublic.h
    INC += H5Gpublic.h
    INC += H5HFpublic.h
    INC += H5HGpublic.h
    INC += H5HLpublic.h
    INC += H5Ipublic.h
    INC += H5Lpublic.h
    INC += H5MMpublic.h
    INC += H5Opublic.h
    INC += H5overflow.h
    INC += H5PLextern.h
    INC += H5PLpublic.h
    INC += H5Ppublic.h
    INC += H5public.h
    INC += H5Rpublic.h
    INC += H5Spublic.h
    INC += H5Tpublic.h
    INC += H5version.h
    INC += H5Zpublic.h
    INC += hdf5.h
    INC += H5pubconf.h
    INC_Linux +=  H5pubconf_32.h
    INC_Linux +=  H5pubconf_64.h

    INC_vxWorks += H5vxWorks.h 

    LIB_SRCS += H5.c
    LIB_SRCS += H5checksum.c
    LIB_SRCS += H5dbg.c
    LIB_SRCS += H5system.c
    LIB_SRCS += H5timer.c
    LIB_SRCS += H5trace.c
    LIB_SRCS += H5A.c
    LIB_SRCS += H5Abtree2.c
    LIB_SRCS += H5Adense.c
    LIB_SRCS += H5Adeprec.c
    LIB_SRCS += H5Aint.c
    LIB_SRCS += H5Atest.c
    LIB_SRCS += H5AC.c
    LIB_SRCS += H5AClog.c
    LIB_SRCS += H5ACdbg.c
    LIB_SRCS += H5ACproxy_entry.c
    LIB_SRCS += H5B.c
    LIB_SRCS += H5Bcache.c
    LIB_SRCS += H5Bdbg.c
    LIB_SRCS += H5B2.c
    LIB_SRCS += H5B2cache.c
    LIB_SRCS += H5B2dbg.c
    LIB_SRCS += H5B2hdr.c
    LIB_SRCS += H5B2int.c
    LIB_SRCS += H5B2internal.c
    LIB_SRCS += H5B2leaf.c
    LIB_SRCS += H5B2stat.c
    LIB_SRCS += H5B2test.c
    LIB_SRCS += H5C.c
    LIB_SRCS += H5Cdbg.c
    LIB_SRCS += H5Cepoch.c
    LIB_SRCS += H5Cimage.c
    LIB_SRCS += H5Clog.c
    LIB_SRCS += H5Cprefetched.c
    LIB_SRCS += H5Cquery.c
    LIB_SRCS += H5Ctag.c
    LIB_SRCS += H5Ctest.c
    LIB_SRCS += H5CS.c
    LIB_SRCS += H5D.c
    LIB_SRCS += H5Dbtree.c
    LIB_SRCS += H5Dbtree2.c
    LIB_SRCS += H5Dchunk.c
    LIB_SRCS += H5Dcompact.c
    LIB_SRCS += H5Dcontig.c
    LIB_SRCS += H5Ddbg.c
    LIB_SRCS += H5Ddeprec.c
    LIB_SRCS += H5Dearray.c
    LIB_SRCS += H5Defl.c
    LIB_SRCS += H5Dfarray.c
    LIB_SRCS += H5Dfill.c
    LIB_SRCS += H5Dint.c
    LIB_SRCS += H5Dio.c
    LIB_SRCS += H5Dlayout.c
    LIB_SRCS += H5Dnone.c
    LIB_SRCS += H5Doh.c
    LIB_SRCS += H5Dscatgath.c
    LIB_SRCS += H5Dselect.c
    LIB_SRCS += H5Dsingle.c
    LIB_SRCS += H5Dtest.c
    LIB_SRCS += H5Dvirtual.c
    LIB_SRCS += H5E.c
    LIB_SRCS += H5Edeprec.c
    LIB_SRCS += H5Eint.c
    LIB_SRCS += H5EA.c
    LIB_SRCS += H5EAcache.c
    LIB_SRCS += H5EAdbg.c
    LIB_SRCS += H5EAdblkpage.c
    LIB_SRCS += H5EAdblock.c
    LIB_SRCS += H5EAhdr.c
    LIB_SRCS += H5EAiblock.c
    LIB_SRCS += H5EAint.c
    LIB_SRCS += H5EAsblock.c
    LIB_SRCS += H5EAstat.c
    LIB_SRCS += H5EAtest.c
    LIB_SRCS += H5F.c
    LIB_SRCS += H5Faccum.c
    LIB_SRCS += H5Fcwfs.c
    LIB_SRCS += H5Fdbg.c
    LIB_SRCS += H5Fdeprec.c
    LIB_SRCS += H5Fefc.c
    LIB_SRCS += H5Ffake.c
    LIB_SRCS += H5Fint.c
    LIB_SRCS += H5Fio.c
    LIB_SRCS += H5Fmount.c
    LIB_SRCS += H5Fquery.c
    LIB_SRCS += H5Fsfile.c
    LIB_SRCS += H5Fspace.c
    LIB_SRCS += H5Fsuper.c
    LIB_SRCS += H5Fsuper_cache.c
    LIB_SRCS += H5Ftest.c
    LIB_SRCS += H5FA.c
    LIB_SRCS += H5FAcache.c
    LIB_SRCS += H5FAdbg.c
    LIB_SRCS += H5FAdblock.c
    LIB_SRCS += H5FAdblkpage.c
    LIB_SRCS += H5FAhdr.c
    LIB_SRCS += H5FAint.c
    LIB_SRCS += H5FAstat.c
    LIB_SRCS += H5FAtest.c
    LIB_SRCS += H5FD.c
    LIB_SRCS += H5FDcore.c
    LIB_SRCS += H5FDfamily.c
    LIB_SRCS += H5FDint.c
    LIB_SRCS += H5FDlog.c
    LIB_SRCS += H5FDmulti.c
    LIB_SRCS += H5FDsec2.c
    LIB_SRCS += H5FDspace.c
    LIB_SRCS += H5FDstdio.c
    LIB_SRCS += H5FDtest.c
    LIB_SRCS += H5FL.c
    LIB_SRCS += H5FO.c
    LIB_SRCS += H5FS.c
    LIB_SRCS += H5FScache.c
    LIB_SRCS += H5FSdbg.c
    LIB_SRCS += H5FSint.c
    LIB_SRCS += H5FSsection.c
    LIB_SRCS += H5FSstat.c
    LIB_SRCS += H5FStest.c
    LIB_SRCS += H5G.c
    LIB_SRCS += H5Gbtree2.c
    LIB_SRCS += H5Gcache.c
    LIB_SRCS += H5Gcompact.c
    LIB_SRCS += H5Gdense.c
    LIB_SRCS += H5Gdeprec.c
    LIB_SRCS += H5Gent.c
    LIB_SRCS += H5Gint.c
    LIB_SRCS += H5Glink.c
    LIB_SRCS += H5Gloc.c
    LIB_SRCS += H5Gname.c
    LIB_SRCS += H5Gnode.c
    LIB_SRCS += H5Gobj.c
    LIB_SRCS += H5Goh.c
    LIB_SRCS += H5Groot.c
    LIB_SRCS += H5Gstab.c
    LIB_SRCS += H5Gtest.c
    LIB_SRCS += H5Gtraverse.c
    LIB_SRCS += H5HF.c
    LIB_SRCS += H5HFbtree2.c
    LIB_SRCS += H5HFcache.c
    LIB_SRCS += H5HFdbg.c
    LIB_SRCS += H5HFdblock.c
    LIB_SRCS += H5HFdtable.c
    LIB_SRCS += H5HFhdr.c
    LIB_SRCS += H5HFhuge.c
    LIB_SRCS += H5HFiblock.c
    LIB_SRCS += H5HFiter.c
    LIB_SRCS += H5HFman.c
    LIB_SRCS += H5HFsection.c
    LIB_SRCS += H5HFspace.c
    LIB_SRCS += H5HFstat.c
    LIB_SRCS += H5HFtest.c
    LIB_SRCS += H5HFtiny.c
    LIB_SRCS += H5HG.c
    LIB_SRCS += H5HGcache.c
    LIB_SRCS += H5HGdbg.c
    LIB_SRCS += H5HGquery.c
    LIB_SRCS += H5HL.c
    LIB_SRCS += H5HLcache.c
    LIB_SRCS += H5HLdbg.c
    LIB_SRCS += H5HLint.c
    LIB_SRCS += H5HLprfx.c
    LIB_SRCS += H5HLdblk.c
    LIB_SRCS += H5HP.c
    LIB_SRCS += H5I.c
    LIB_SRCS += H5Itest.c
    LIB_SRCS += H5L.c
    LIB_SRCS += H5Lexternal.c
    LIB_SRCS += H5MF.c
    LIB_SRCS += H5MFaggr.c
    LIB_SRCS += H5MFdbg.c
    LIB_SRCS += H5MFsection.c
    LIB_SRCS += H5MM.c
    LIB_SRCS += H5MP.c
    LIB_SRCS += H5MPtest.c
    LIB_SRCS += H5O.c
    LIB_SRCS += H5Oainfo.c
    LIB_SRCS += H5Oalloc.c
    LIB_SRCS += H5Oattr.c
    LIB_SRCS += H5Oattribute.c
    LIB_SRCS += H5Obogus.c
    LIB_SRCS += H5Obtreek.c
    LIB_SRCS += H5Ocache.c
    LIB_SRCS += H5Ocache_image.c
    LIB_SRCS += H5Ochunk.c
    LIB_SRCS += H5Ocont.c
    LIB_SRCS += H5Ocopy.c
    LIB_SRCS += H5Odbg.c
    LIB_SRCS += H5Odrvinfo.c
    LIB_SRCS += H5Odtype.c
    LIB_SRCS += H5Oefl.c
    LIB_SRCS += H5Ofill.c
    LIB_SRCS += H5Oflush.c
    LIB_SRCS += H5Ofsinfo.c
    LIB_SRCS += H5Oginfo.c
    LIB_SRCS += H5Olayout.c
    LIB_SRCS += H5Olinfo.c
    LIB_SRCS += H5Olink.c
    LIB_SRCS += H5Omessage.c
    LIB_SRCS += H5Omtime.c
    LIB_SRCS += H5Oname.c
    LIB_SRCS += H5Onull.c
    LIB_SRCS += H5Opline.c
    LIB_SRCS += H5Orefcount.c
    LIB_SRCS += H5Osdspace.c
    LIB_SRCS += H5Oshared.c
    LIB_SRCS += H5Oshmesg.c
    LIB_SRCS += H5Ostab.c
    LIB_SRCS += H5Otest.c
    LIB_SRCS += H5Ounknown.c
    LIB_SRCS += H5P.c
    LIB_SRCS += H5Pacpl.c
    LIB_SRCS += H5Pdapl.c
    LIB_SRCS += H5Pdcpl.c
    LIB_SRCS += H5Pdeprec.c
    LIB_SRCS += H5Pdxpl.c
    LIB_SRCS += H5Pencdec.c
    LIB_SRCS += H5Pfapl.c
    LIB_SRCS += H5Pfcpl.c
    LIB_SRCS += H5Pfmpl.c
    LIB_SRCS += H5Pgcpl.c
    LIB_SRCS += H5Pint.c
    LIB_SRCS += H5Plapl.c
    LIB_SRCS += H5Plcpl.c
    LIB_SRCS += H5Pocpl.c
    LIB_SRCS += H5Pocpypl.c
    LIB_SRCS += H5Pstrcpl.c
    LIB_SRCS += H5Ptest.c
    LIB_SRCS += H5PB.c
    LIB_SRCS += H5PL.c
    LIB_SRCS += H5R.c
    LIB_SRCS += H5Rdeprec.c
    LIB_SRCS += H5UC.c
    LIB_SRCS += H5RS.c
    LIB_SRCS += H5S.c
    LIB_SRCS += H5Sall.c
    LIB_SRCS += H5Sdbg.c
    LIB_SRCS += H5Shyper.c
    LIB_SRCS += H5Snone.c
    LIB_SRCS += H5Spoint.c
    LIB_SRCS += H5Sselect.c
    LIB_SRCS += H5Stest.c
    LIB_SRCS += H5SL.c
    LIB_SRCS += H5SM.c
    LIB_SRCS += H5SMbtree2.c
    LIB_SRCS += H5SMcache.c
    LIB_SRCS += H5SMmessage.c
    LIB_SRCS += H5SMtest.c
    LIB_SRCS += H5ST.c
    LIB_SRCS += H5T.c
    LIB_SRCS += H5Tarray.c
    LIB_SRCS += H5Tbit.c
    LIB_SRCS += H5Tcommit.c
    LIB_SRCS += H5Tcompound.c
    LIB_SRCS += H5Tconv.c
    LIB_SRCS += H5Tcset.c
    LIB_SRCS += H5Tdbg.c
    LIB_SRCS += H5Tdeprec.c
    LIB_SRCS += H5Tenum.c
    LIB_SRCS += H5Tfields.c
    LIB_SRCS += H5Tfixed.c
    LIB_SRCS += H5Tfloat.c
    LIB_SRCS += H5Tnative.c
    LIB_SRCS += H5Toffset.c
    LIB_SRCS += H5Toh.c
    LIB_SRCS += H5Topaque.c
    LIB_SRCS += H5Torder.c
    LIB_SRCS += H5Tpad.c
    LIB_SRCS += H5Tprecis.c
    LIB_SRCS += H5Tstrpad.c
    LIB_SRCS += H5Tvisit.c
    LIB_SRCS += H5Tvlen.c
    LIB_SRCS += H5TS.c
    LIB_SRCS += H5VM.c
    LIB_SRCS += H5WB.c
    LIB_SRCS += H5Z.c
    LIB_SRCS += H5Zdeflate.c
    LIB_SRCS += H5Zfletcher32.c
    LIB_SRCS += H5Znbit.c
    LIB_SRCS += H5Zscaleoffset.c
    LIB_SRCS += H5Zshuffle.c
    LIB_SRCS += H5Zszip.c
    LIB_SRCS += H5Ztrans.c

    # H5Tinit.c is architecture specific
    LIB_SRCS += H5Tinit.c

    LIB_SRCS_vxWorks += H5vxWorks.c

    # This file allows printing how the library was configured.
    # It is not yet correct for each system.
    LIB_SRCS += H5lib_settings.c

    ifeq ($(SZIP_EXTERNAL),YES)
      ifdef SZIP_INCLUDE
        USR_INCLUDES += $(SZIP_INCLUDE)
      endif
      ifdef SZIP_LIB
        sz_DIR       = $(SZIP_LIB)
        LIB_LIBS     += sz
      else
        LIB_SYS_LIBS += sz
      endif
    else
      LIB_LIBS += szip
    endif

    ifeq ($(ZLIB_EXTERNAL),YES)
      ifdef ZLIB_INCLUDE
        USR_INCLUDES += $(ZLIB_INCLUDE)
      endif
      ifdef ZLIB_LIB
        z_DIR        = $(ZLIB_LIB)
        LIB_LIBS     += z
      else
        LIB_SYS_LIBS += z
      endif
    else
      LIB_LIBS += zlib
    endif

    LIB_SYS_LIBS_WIN32 += ws2_32

    H5detect_SRCS += H5detect.c
    PROD_SYS_LIBS_WIN32 += ws2_32

  endif # ($(HDF5_EXTERNAL),NO)
endif # ($(WITH_HDF5),YES)

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

