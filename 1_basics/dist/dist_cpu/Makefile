NVCC = /usr/local/cuda-8.0/bin/nvcc
NVCC_FLAGS = -g -G -Xcompiler -Wall

all: main.exe

main.exe: main.o aux_function.o
	$(NVCC) $^ -o $@

main.o: main.cpp aux_function.h
	$(NVCC) $(NVCC_FLAGS) -c $< -o $@

aux_function: aux_function.cpp aux_function.h
	$(NVCC) $(NVCC_FLAGS) -c $< -o $@