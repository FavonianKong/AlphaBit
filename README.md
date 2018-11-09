# AlphaBit
It's a store and query system for large scale RDF graph.

Dependency:
-----------
Please install boost, you can use the following version or other version [boost_1_65_0.tar.gz](https://dl.bintray.com/boostorg/release/1.65.0/source/) The following are the commands to install boost.<br>
```
tar -zxvf boost_1_65_0.tar.gz
cd boost_1_65_0
./bootstrap.sh
./bjam
cp -r boost/ /usr/local/include/
```
You should also install tcmalloc which is included in [gperftools](https://github.com/gperftools/gperftools).<br>
```
tar zxvf gperftools-2.7.tar.gz
cd gperftools-2.7
./configure --prefix=/usr/local
make
make install
```

Building:
---------
AlphaBit must be build using GNU make and a reasonable C++ compiler,Also it should support `c++11`. Ideally a simple  "`make`" is enough, it will build the tree high-level executables in bin/lrelease/.

Using:
------
AlphaBit currently includes two executables. The first (buildTripleBitFromN3)
is used to build a new database from an turtle/ntriples input: <br>
```
buildTripleBitFromN3 mydata.n3 database_directory
```
After loading the database can be queried with triplebitQuery: <br>
```
triplebitQuery database_directory query_directory
```
The program shows a command prompt and accept SPARQL queries.<br>
