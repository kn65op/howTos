# Variables

```
EXIV_DIRECTORY="" # path to manually build clone exiv
DARKTABLE_DIRECTORY="" # path to darktable clone
INSTALL_DIR="" # path to installation directory
```

# Build

```
cmake ../ -GNinja -DCMAKE_BUILD_TYPE=Release -DCMAKE_CXX_COMPILER=g++-8 -DCMAKE_C_COMPILER=gcc-8 -DCMAKE_LIBRARY_PATH=${EXIV_DIRECTORY}/build/lib/ -DCMAKE_PREFIX_PATH="${EXIV_DIRECTORY}/build/lib;${EXIV_DIRECTORY}" -DCMAKE_INSTALL_PREFIX=${INSTALL_DIR}
```

Ensure that ```EXIV2_INCLUDE_DIR``` and ```EXIV2_LIBRARY``` in ```CMakeCache.txt``` points to the same checkout or system library.


# Run
```
export LD_LIBRARY_PATH=${DARKTABLE_DIRECTORY}/build/src:${EXIV_DIRECTORY}/build/lib/
```
