SET(MAGS_SOURCES mBc.cpp mb.cpp m_B.cpp mb_idc.cpp Mjma.cpp ML.cpp MLv.cpp ML_idc.cpp Ms20.cpp msbb.cpp Mwp.cpp)
SET(MAGS_HEADERS mBc.h mb.h m_B.h Mjma.h ML.h MLv.h Ms20.h msbb.h Mwp.h)

FILE(GLOB descs "${CMAKE_CURRENT_SOURCE_DIR}/descriptions/*.xml")
INSTALL(FILES ${descs} DESTINATION ${SC3_PACKAGE_APP_DESC_DIR})

SET(IDC_DATA data/qfvc.mb data/global.ml)
SC_INSTALL_DATA(IDC "magnitudes/IDC")

SC_SETUP_LIB_SUBDIR(MAGS)
