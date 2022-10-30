cmake_minimum_required(VERSION 3.10)
project(cutest 
    VERSION 1.0.0
    LANGUAGES C
)


# configure_file(manifest.h.in manifest.h)


# set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -D_GNU_SOURCE=1")


# include_directories(
#     ${PROJECT_SOURCE_DIR}
#     ${PROJECT_BINARY_DIR}
# )


# Install
install(FILES cutest.h DESTINATION "include")


# CPack
set(CPACK_PACKAGE_FILE_NAME "libcutest-${PROJECT_VERSION}")
set(CPACK_SET_DESTDIR true)
set(CPACK_PACKAGE_NAME libcutest)
set(CPACK_PACKAGE_CONTACT "Vahid Mardani <vahid.mardani@gmail.com>")
set(CPACK_GENERATOR DEB)
include(CPack)
