cmake_minimum_required(VERSION 3.7)
project(cutest 
    VERSION 1.2.0
    LANGUAGES C
)


# Install
install(FILES cutest.h DESTINATION "include")


# CPack
set(CPACK_PACKAGE_FILE_NAME "libcutest-${PROJECT_VERSION}")
set(CPACK_SET_DESTDIR true)
set(CPACK_PACKAGE_NAME libcutest)
set(CPACK_PACKAGE_CONTACT "Vahid Mardani <vahid.mardani@gmail.com>")
set(CPACK_GENERATOR DEB)
include(CPack)
