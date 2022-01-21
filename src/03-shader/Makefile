


CXX = g++

CXXFLAGS := -std=c++17 -Wall -Wextra -g
LIBRARIES	:= -lglad -lglfw3dll

INCLUDE	:= ../../include
INCLUDEDIRS	:= $(INCLUDE)
INCLUDES	:= $(patsubst %,-I%, $(INCLUDEDIRS:%/=%))

LIB		:= ../../lib
LIBDIRS		:= $(LIB)
LIBS		:= $(patsubst %,-L%, $(LIBDIRS:%/=%))


all: $(patsubst %.cpp, %.exe, $(wildcard *.cpp))

%.exe: %.cpp Makefile
	$(CXX) $(CXXFLAGS) $(INCLUDES) $< -o $@ $(LIBS) $(LIBRARIES)

clean: rm *.exe