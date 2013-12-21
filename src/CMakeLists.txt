
ADD_SUBDIRECTORY( data )

SET( fishplayer_SRCS
    mainwindow.cpp
)

KDE4_ADD_KCFG_FILES( fishplayer_SRCS fishplayer.kcfgc )

KDE4_ADD_KDEINIT_EXECUTABLE( fishplayer ${fishplayer_SRCS} main.cpp )

INSTALL( TARGETS fishplayer ${INSTALL_TARGETS_DEFAULT_ARGS} )

INSTALL( FILES fishplayer.kcfg  DESTINATION  ${KCFG_INSTALL_DIR} )
INSTALL( FILES fishplayerui.rc  DESTINATION  ${DATA_INSTALL_DIR}/fishplayer )
