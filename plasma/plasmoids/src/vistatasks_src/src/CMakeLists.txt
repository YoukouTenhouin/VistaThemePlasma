# TODO: adapt "org.kde.plasma" here & elsewhere if needed (see README)
add_definitions(-DTRANSLATION_DOMAIN=\"plasma_applet_io.gitgud.catpswin56.vistatasks\")
remove_definitions(-DQT_NO_CAST_FROM_ASCII)


set(vistatasks_SRCS
    seventasks.cpp
)

add_library(io.gitgud.catpswin56.vistatasks MODULE ${vistatasks_SRCS})

target_link_libraries(io.gitgud.catpswin56.vistatasks
                      Qt6::Gui
                      Qt6::Quick
                      KF6::I18n
                      KF6::WindowSystem
                      Plasma::Plasma
                      Plasma::PlasmaQuick
                      KF6::Svg
                      KF6::ConfigCore
                      KF6::ConfigGui
                      KF6::CoreAddons
                      KF6::KirigamiPlatform)

install(TARGETS io.gitgud.catpswin56.vistatasks DESTINATION ${KDE_INSTALL_PLUGINDIR}/plasma/applets)


#plasma_install_package(package io.gitgud.wackyideas.seventasks)
