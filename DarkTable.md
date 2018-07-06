# Varibales

```
EXIV_DIRECTORY="" #path to manually build clone exiv
DARKTABLE_DIRECTORY="" #path to darktable clone
```

# Build
```
cmake ../ -DCMAKE_CXX_COMPILER=g++-8 -DCMAKE_LIBRARY_PATH=${EXIV_DIRECTORY}/build/lib/ -DCMAKE_PREFIX_PATH=${EXIV_DIRECTORY}/build/lib # one of them is probably not required
```


# Run
```
export LD_LIBRARY_PATH=${DARKTABLE_DIRECTORY}/build/src:${EXIV_DIRECTORY}/build/lib/
```
