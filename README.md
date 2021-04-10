# FT-SZ
SDC Resilient Error-bounded Lossy Compressor




It is the fault tolerant version of SZ (https://github.com/disheng222/SZ).
So please follow the installation of SZ "README", but please remember to use --enable-randomaccess option to compile the package.
You can do this when you do configure: ./configure --prefix=xxx --enable-randomaccess.


After installation, you can go to example diretory to run some examples like following:
[xxx example]$ sz -z -f -c sz.config -i testdata/x86/testfloat_8_8_128.dat -3 8 8 128
calls rdac compression
2048500 dup err: 0
machine epsilon count: 0
compression time = 0.030005
compressed data file: testdata/x86/testfloat_8_8_128.dat.sz
[xxx example]$ sz -x -f -i testdata/x86/testfloat_8_8_128.dat -s testdata/x86/testfloat_8_8_128.dat.sz -3 8 8 128 4 4 4 8 8 8 -a
decompress with random access how about this time
1056740212138 1055206705957 1063707853260 1051805280021 1060994263175 1061174356232 1050569638067 1064724454096 1056740212138 1055206705957 
1056740212138 Min=0.21328493952751159668, Max=5.0532207489013671875, range=4.8399357795715332031
Max absolute error = 0.0009477735
Max relative error = 0.000196
compressionRatio=25.801575
decompression time = 0.001859 seconds.
decompressed data file: testdata/x86/testfloat_8_8_128.dat.sz.out