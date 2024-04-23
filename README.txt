# grpcHelloWorld
A HelloWorld Project adding grpc functionality using CMake

# Step one
Clone the grpc repo using this command: git clone --recurse-submodules -b v1.62.0 --depth 1 --shallow-submodules https://github.com/grpc/grpc

# Step two
Install grpc on your system using the following commands:
$ cd grpc
$ mkdir -p cmake/build
$ pushd cmake/build
$ cmake -DgRPC_INSTALL=ON \
      -DgRPC_BUILD_TESTS=OFF \
      -DCMAKE_INSTALL_PREFIX=$MY_INSTALL_DIR \
      ../..
$ make -j 4
$ make install
$ popd

# Step three
Create a project folder and create a subfolder called "cmake" inside that folder 

# Step four
Copy the file common.cmake into the cmake folder 

# Step Five
copy the following files into the project folder
  * helloworld.proto
  * greeter_client.cc
  * greeeter_server.cc
  * CMakeLists.txt
    
# Step six
create a folder called "build" inside the main project folder

# Stepp seven
cd build/
cmake .. 
cmake --build .

