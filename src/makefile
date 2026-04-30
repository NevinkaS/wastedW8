# Default target
all: outputs/program

# Link the object files to create the final executable
outputs/program: outputs/main.o outputs/stats.o
	gcc outputs/main.o outputs/stats.o -o outputs/program

# Compile main.c into an object file
outputs/main.o: src/main.c src/stats.h
	gcc -c src/main.c -o outputs/main.o

# Compile stats.c into an object file
outputs/stats.o: src/stats.c src/stats.h
	gcc -c src/stats.c -o outputs/stats.o

# Cleaner
clean:
	rm -f outputs/*.o outputs/program outputs/test_runner