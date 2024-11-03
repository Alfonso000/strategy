# cmake_minimum_required(VERSION 3.10)
# # Establecer la política para OpenGL
# cmake_policy(SET CMP0072 NEW)

# project(strategy)



# set(CMAKE_CXX_STANDARD 17)
# set(CMAKE_C_STANDARD_REQUIRED True)

# set(SOURCE src/main.cpp)

# # # Incluir directorios de OpenGL y otras librerías
# find_package(OpenGL REQUIRED)
# find_package(GLM REQUIRED)
# find_package(GLFW REQUIRED)


# add_executable( stra ${SOURCES})


# # Añadir archivos fuente y directorios de inclusión
# include_directories(${OPENGL_INCLUDE_DIRS} ${GLM_INCLUDE_DIRS} ${GLFW3_INCLUDE_DIRS})

# # Enlazar librerías
# target_link_libraries(strategy ${OPENGL_LIBRARIES} ${GLFW_LIBRARIES} glm)

# CMake mínimo requerido
cmake_minimum_required(VERSION 3.10)

# Establecer la política para OpenGL
cmake_policy(SET CMP0072 NEW)

# Nombre del proyecto
project(strategy)

# Especificar el estándar de C++
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Buscar las bibliotecas necesarias
find_package(OpenGL REQUIRED)
# find_package(GLFW REQUIRED)

# Archivos fuente
set(SOURCES
    src/main.cpp
)

# Crear el ejecutable
add_executable(juego ${SOURCES})

# Enlazar las bibliotecas necesarias
target_link_libraries(juego
    ${OPENGL_LIBRARIES}
    # ${GLFW_LIBRARIES}
)

# Incluir directorios
include_directories(${OPENGL_INCLUDE_DIR} "/usr/include/GLFW" "/usr/include/glm")