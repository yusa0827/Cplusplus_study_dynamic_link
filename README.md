# 概要
ダイナミックリンク、スタティックリンクを学びたい


# 流れ
1. ソースコードcpp(lib_hello.cpp) から オブジェクトファイルo を作成する
   1. g++ -c hello.cpp
   2. hello.o が作成される
2. オブジェクトファイルo から 共有ライブラリを作成する 
   1. g++ -shared -o lib_hello.dll hello.o
   2. lib_hello.dll が作成される
3. ソースコードcpp(hello.cpp) のヘッダーh(hello.h)
4. コンパイルするときに、ダイナミックリンクライブラリ(lib_hello.dll)をリンク
   1. g++ -I./ -L./ -o main.exe main.cpp -llib_hello
   2. main.exe が作成できた
   3. main.exe を実行する


# [参考] Cygwin上でgccでdllにコンパイルする。
https://blog.katty.in/4350#toc3

