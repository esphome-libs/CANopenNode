# ESP-IDF component build; the same sources as library.json. The application provides the CAN driver functions.
if(ESP_PLATFORM)
  file(GLOB CANOPENNODE_SRCS
    "${CMAKE_CURRENT_LIST_DIR}/CANopen.c"
    "${CMAKE_CURRENT_LIST_DIR}/301/*.c"
    "${CMAKE_CURRENT_LIST_DIR}/303/*.c"
    "${CMAKE_CURRENT_LIST_DIR}/304/*.c"
    "${CMAKE_CURRENT_LIST_DIR}/305/*.c"
    "${CMAKE_CURRENT_LIST_DIR}/309/*.c"
    "${CMAKE_CURRENT_LIST_DIR}/extra/*.c"
    "${CMAKE_CURRENT_LIST_DIR}/storage/CO_storage.c")
  idf_component_register(SRCS ${CANOPENNODE_SRCS} INCLUDE_DIRS ".")
endif()
