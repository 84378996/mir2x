AUX_SOURCE_DIRECTORY(. NPCWIL2PNG_SRC)
ADD_EXECUTABLE(npcwil2png ${NPCWIL2PNG_SRC})
ADD_DEPENDENCIES(npcwil2png mir2x_3rds)

TARGET_INCLUDE_DIRECTORIES(npcwil2png PRIVATE ${MIR2X_COMMON_SOURCE_DIR})
TARGET_INCLUDE_DIRECTORIES(npcwil2png PRIVATE ${CMAKE_CURRENT_BINARY_DIR})
TARGET_INCLUDE_DIRECTORIES(npcwil2png PRIVATE ${CMAKE_CURRENT_LIST_DIR})

TARGET_LINK_LIBRARIES(npcwil2png ${CMAKE_DL_LIBS})
TARGET_LINK_LIBRARIES(npcwil2png common          )
TARGET_LINK_LIBRARIES(npcwil2png ${PNG_LIBRARIES}        )
