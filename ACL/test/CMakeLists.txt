add_subdirectory("Transport")

set(LIBRARIES ACL ${CMAKE_THREAD_LIBS_INIT} ACLTransportCommonTestLib)
set(INCLUDE_PATH
    "${AVSCommon_INCLUDE_DIRS}"
    "${ACL_SOURCE_DIR}/include"
    "${AVSCommon_SOURCE_DIR}/AVS/test"
    "${AVSCommon_SOURCE_DIR}/SDKInterfaces/test"
    "${AVSCommon_SOURCE_DIR}/Utils/test")
discover_unit_tests("${INCLUDE_PATH}" "${LIBRARIES}")
