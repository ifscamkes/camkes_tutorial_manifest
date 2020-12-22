cmake_minimum_required(VERSION 3.7.2)

project(hello-camkes-1 C)

DeclareTutorialsCAmkESComponent(Bidder1 TEMPLATE_SOURCES components/Bidder1/src/bidder1.c)
DeclareTutorialsCAmkESComponent(Bidder2 TEMPLATE_SOURCES components/Bidder2/src/bidder2.c)
DeclareTutorialsCAmkESComponent(Bidder3 TEMPLATE_SOURCES components/Bidder3/src/bidder3.c)
DeclareTutorialsCAmkESComponent(Auctioner TEMPLATE_SOURCES components/Auctioner/src/auctioner.c)
DeclareTutorialsCAmkESComponent(RWFM_MONITOR TEMPLATE_SOURCES components/RWFM_MONITOR/src/rwfm_monitor.c)

DeclareCAmkESComponent(EmptyComponent)

DeclareTutorialsCAmkESRootserver(hello-camkes-1.camkes ADL_IS_TEMPLATE
    TEMPLATE_SOURCES interfaces/MakeBid.camkes interfaces/DeclareResult.camkes interfaces/RWFM_P.camkes
    TUTORIAL_SOURCES components/Bidder1/Bidder1.camkes components/Bidder2/Bidder2.camkes components/Bidder3/Bidder3.camkes components/Auctioner/Auctioner.camkes components/RWFM_MONITOR/RWFM_MONITOR.camkes
)
