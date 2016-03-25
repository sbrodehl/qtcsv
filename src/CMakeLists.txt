set(LIBNAME "QtCSV")

# Find the QtWidgets library
find_package(Qt5Core)

SET(SOURCE_FILES
        include/abstractdata.h
        include/qtcsv_global.h
        include/reader.h
        include/stringdata.h
        include/variantdata.h
        include/writer.h
        sources/contentiterator.cpp
        sources/contentiterator.h
        sources/filechecker.h
        sources/reader.cpp
        sources/stringdata.cpp
        sources/symbols.h
        sources/variantdata.cpp
        sources/writer.cpp)

add_library(${LIBNAME} ${SOURCE_FILES})

target_link_libraries(${LIBNAME}
        Qt5::Core)