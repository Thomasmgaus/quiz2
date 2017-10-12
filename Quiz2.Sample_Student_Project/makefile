all: build
all: clean
all: archive
all: doc

build: collegemain.o college.o course.o
	g++ collegemain.o college.o course.o -o myexe
doc:
	doxygen *.cc
archive:
	tar -cvf quiz2.tar myexe collegemain.cc college.cc college.h course.cc course.h makefile node.h tarray.h html latex 2401fal15proj3.doc
clean:
	rm *o
collegemain.o:collegemain.cc
	g++ -c collegemain.cc college.h node.h course.h college.cc course.cc
college.o: college.cc
	g++ -c college.cc college.h
course.o: course.cc
	g++ -c course.cc course.h
