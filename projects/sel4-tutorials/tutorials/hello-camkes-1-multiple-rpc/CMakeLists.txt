cmake_minimum_required(VERSION 3.7.2)

project(hello-camkes-1 C)

DeclareTutorialsCAmkESComponent(Client1 TEMPLATE_SOURCES components/Client1/src/client1.c)
DeclareTutorialsCAmkESComponent(Client2 TEMPLATE_SOURCES components/Client2/src/client2.c)
DeclareTutorialsCAmkESComponent(Echo TEMPLATE_SOURCES components/Echo/src/echo.c)
DeclareTutorialsCAmkESComponent(RWFM_MONITOR TEMPLATE_SOURCES components/RWFM_MONITOR/src/rwfm_monitor.c)

DeclareCAmkESComponent(EmptyComponent)

DeclareTutorialsCAmkESRootserver(hello-camkes-1.camkes ADL_IS_TEMPLATE
    TEMPLATE_SOURCES interfaces/HelloSimple.camkes interfaces/HelloSimple1.camkes interfaces/RWFM_P.camkes
    TUTORIAL_SOURCES components/Client1/Client1.camkes components/Client2/Client2.camkes components/Echo/Echo.camkes components/RWFM_MONITOR/RWFM_MONITOR.camkes
)
