
all: clean bc opt


bc:
	clang -Xclang -disable-O0-optnone -emit-llvm -o test.bc -S -c test.c
#	llvm-dis test.bc

opt:
	opt -disable-opt -mem2reg -S test.bc -o test-mem2reg.ll

clean:
	rm -f test.bc *.ll
