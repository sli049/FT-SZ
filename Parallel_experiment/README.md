1. replace the sz path and ftrsz path with your own installation directory in the compile.sh file
2. compile the paralell code: bash compile.sh
3. run the ft version and non-ft version: mpirun -n 2 ./parallel_sz_ft sz.config 6 512 512 512
