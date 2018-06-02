PYTHON_VERSION = 2.7
PYTHON_INCLUDE = /usr/include/python$(PYTHON_VERSION)
BOOST_INC = /usr/include
BOOST_LIB = /usr/lib/x86_64-linux-gnu
OPENCV_LIB = $$(pkg-config --libs opencv)
OPENCV_INC = $$(pkg-config --cflags opencv)
NUMPY_INCLUDE = /usr/lib/python$(PYTHON_VERSION)/site-packages/numpy/core/include

all:
	g++ -ggdb -I$(PYTHON_INCLUDE) -I$(NUMPY_INCLUDE) -I$(BOOST_INC) $(OPENCV_CFLAGS) -fPIC -c -std=c++11 iksolver.cpp
	g++ -shared iksolver.o -o iksolver.so -L$(BOOST_LIB) -lboost_python -L/usr/lib/python$(PYTHON_VERSION)/config -lpython$(PYTHON_VERSION)
