# HOT Usage Sample

Sample project showing the use of the Height Optimized Trie (HOT).
It integrates HOT's source repository (https://github.com/speedskater/hot) as a git submodule and contains a CMake based build, which directly uses the HOT source repository
by calling `ADD_SUBDIRECTORY`.

# The Sample Project

The sample project itself is contained in the directory '/sample/'.
It uses:
    * the single threaded HOT implementation <hot/singlethreaded/HOTSingleThreaded.hpp>
    * the identity key extractor, which trivially maps a value to itself <idx/contenthelpers/IdentityKeyExtractor.hpp>

Therefore, the sample links against "hot-single-threaded-lib" and "content-helpers-lib" by calling
`target_link_libraries(sample hot-single-threaded-lib content-helpers-lib)` in its CMakeLists.txt


# Compiling and Runnig the sample:
```
git clone https://github.com/speedskater/hot-sample.git hot-sample
cd hot-sample
git submodule update --init --recursive
mkdir build
cd build
cmake ../
make
./sample/sample
```


