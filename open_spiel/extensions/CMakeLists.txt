# Json package required for extensions
find_package(nlohmann_json 3.2.0 REQUIRED)

add_library (extensions OBJECT
  global_variables.h
  utils.h
  algorithms.h
  algorithms.cc
  poker_methods.h
  #poker_methods.cc
)

target_link_libraries(extensions PRIVATE nlohmann_json::nlohmann_json)

target_include_directories (extensions PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

#add_executable(name_test name_test.cc
#    $<TARGET_OBJECTS:algorithms> ${OPEN_SPIEL_OBJECTS})
#add_test(name_test name_test)

