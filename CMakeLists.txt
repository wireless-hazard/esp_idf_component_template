set(COMPONENT_SRCS
    "src/lib_source.cpp")

set(COMPONENT_ADD_INCLUDEDIRS "include")

set(COMPONENT_PRIV_REQUIRES main)

register_component(esp_idf_component_template)

component_compile_options(PUBLIC -DMPU_COMPONENT_TRUE=1)
