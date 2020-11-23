CC=g++ -mbmi -msse2 -w
CFLAGS = -std=c++11 -O3 -g
OBJS=main.cpp test.o factor.o
all: SketchTest 
../sketch/sketchList.h:
	sh genSketchList.sh
test.o: test.cpp
	$(CC) $(CFLAGS) -c test.cpp
factor.o: factor.cpp
	$(CC) $(CFLAGS) -c factor.cpp
SketchTest: main.cpp test.o factor.o ../sketch/sketchList.h
	$(CC) $(CFLAGS) $(OBJS) -o $@
	@echo "Compile successfully!"
	rm ../sketch/sketchList.h
	rm *.o
clean :
	rm -rf SketchTest *.o
