CMAKE_MINIMUM_REQUIRED( VERSION 2.8 )

SET(
	PROJECT_NAME
	"TestApp"
)

SET(
	PROJECT_SOURCES
	"../DesktopApp.cpp"
)

SET(
	PROJECT_INCLUDES
	"../../../lib/include"
)

SET(
	PROJECT_LIBRARIES
	"lifeline"
	"sfml-graphics"
	"sfml-window"
	"sfml-system"
)

#----------- DO NOT EDIT BELOW --------------

INCLUDE_DIRECTORIES( ${PROJECT_INCLUDES} )
ADD_EXECUTABLE( ${PROJECT_NAME} ${PROJECT_SOURCES} )
TARGET_LINK_LIBRARIES( ${PROJECT_NAME} ${PROJECT_LIBRARIES} )

INCLUDE_DIRECTORIES( ${PROJECT_INCLUDES} )
ADD_EXECUTABLE( "SymbolFileMaker" "../SymbolFileMaker.cpp" )
TARGET_LINK_LIBRARIES( "SymbolFileMaker" "lifeline" )
