target_add_lib(hf3fs_api client-lib-common storage-client numa rt)

add_library(usrbio STATIC
    $<TARGET_OBJECTS:hf3fs_api>
    $<TARGET_OBJECTS:client-lib-common>
    $<TARGET_OBJECTS:core-user-fbs>
    $<TARGET_OBJECTS:common>
    $<TARGET_OBJECTS:fmt>
    $<TARGET_OBJECTS:scn::scn>
)