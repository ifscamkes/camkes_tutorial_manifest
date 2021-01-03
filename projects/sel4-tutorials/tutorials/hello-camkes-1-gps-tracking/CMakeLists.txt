cmake_minimum_required(VERSION 3.7.2)

project(hello-camkes-1 C)

DeclareTutorialsCAmkESComponent(GPS TEMPLATE_SOURCES components/GPS/src/gps.c)
DeclareTutorialsCAmkESComponent(Server TEMPLATE_SOURCES components/Server/src/server.c)
DeclareTutorialsCAmkESComponent(Intruder TEMPLATE_SOURCES components/Intruder/src/intruder.c)
DeclareTutorialsCAmkESComponent(RWFM_MONITOR TEMPLATE_SOURCES components/RWFM_MONITOR/src/rwfm_monitor.c)

DeclareTutorialsCAmkESRootserver(hello-camkes-1.camkes ADL_IS_TEMPLATE
    TEMPLATE_SOURCES interfaces/ProvideDirections.camkes interfaces/ProvideDetails.camkes interfaces/RWFM_P.camkes
    TUTORIAL_SOURCES components/GPS/GPS.camkes components/Server/Server.camkes components/Intruder/Intruder.camkes components/RWFM_MONITOR/RWFM_MONITOR.camkes
)
