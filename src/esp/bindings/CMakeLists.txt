set(MODULE_NAME "habitat_sim_bindings")

pybind11_add_module(habitat_sim_bindings bindings.cpp ShortestPathBindings.cpp)
target_link_libraries(habitat_sim_bindings
  PUBLIC
    agent
    assets
    scene
    core
    gfx
    nav
    sensor
)

# target_include_directories(environment
#   PUBLIC
#     ${CMAKE_CURRENT_LIST_DIR}
# )

# file(WRITE ${PYTHON_ROOT}/libpath.py "LIB_PATH='${CMAKE_CURRENT_BINARY_DIR}'\n")
