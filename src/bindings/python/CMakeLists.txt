if(SIP_IS_GOOD)
include(SIPMacros)

include_directories(
  ${SIP_INCLUDE_DIR}
  ${PYTHON_INCLUDE_PATH}
  ${CMAKE_SOURCE_DIR}/src
  ${EIGEN2_INCLUDE_DIR})

file(GLOB SIP_FILES "${CMAKE_CURRENT_SOURCE_DIR}/*.sip")
set(SIP_INCLUDES ${SIP_FILES})
add_sip_python_module(PyKDL ./PyKDL.sip orocos-kdl)
#set(SIP_EXTRA_FILES_DEPEND ${SIP_FILES})
endif(SIP_IS_GOOD)