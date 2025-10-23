set(headers_ixx

)

set(headers

)

set(sources
 ${CMAKE_CURRENT_SOURCE_DIR}/xsd.cxx

)

source_group(TREE ${CMAKE_CURRENT_SOURCE_DIR} FILES ${headers} ${headers_ixx} ${sources})

add_executable(xsd)

target_sources(xsd
 PRIVATE
 ${sources}
 ${headers_ixx}
 ${headers}
)

#set_source_files_properties(${headers_ixx} PROPERTIES HEADER_FILE_ONLY TRUE)

target_include_directories(xsd
 PRIVATE
 $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/..>
)

target_link_libraries(xsd
PRIVATE XercesC::XercesC
)