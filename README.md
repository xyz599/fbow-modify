修复同一底库训练出词袋不同问题；
添加获取单词数、词典训练层数接口；
修复单词的id 大于总单词数的问题；
修复 调用transform（features，level，fBoW，fBoW2）
    与调用fBoW=transform（features），
    fBoW结果不一致问题；

FBOW
=====
FBOW (Fast Bag of Words) is an extremmely optimized version of the DBow2/DBow3 libraries. The library is highly optimized to speed up the Bag of Words creation using  AVX,SSE and MMX instructions. In loading a vocabulary, fbow is ~80x faster than DBOW2 (see tests directory and try). In transforming an image into a bag of words using on machines with AVX instructions, it is ~6.4x faster.

## 
## Main features:
	* Only depends on OpenCV 
	* Any type of descriptors allowed out of the box (binary and real)
	* Dictionary creation from a set of images. Bugs found in DBOW2/3 corrected.
	* Extremmely fast bow creation using specialized versions using AVX,SSE and MMX instructions both for binary and floating point descriptors.
	* Very fast load of vocabularies

## 
## The main differences with DBOW2/3 are:

	* Not yet implemented indexing of images. 

##
## Citing

If you use this project in academic research you must cite us. This project is part of the ucoslam project. Visit [ucoslam.com](http://ucoslam.com) for more information


##
## Vocabularies

In directory vocabularies you have one already prepared for orb.
##
## Test speed
 Go to test and run the program test_dbow2VSfbow
##
## License
This software is distributed under MIT License
