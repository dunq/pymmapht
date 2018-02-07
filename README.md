# pymmapht
* A mmap hashtable in python, with compact space use.
* Derived from [pyshmht](https://github.com/felix021/pyshmht.git).
* Can be useful for python http servers, e.g. tornado, and data processing with multiple processes.
* Limititaions: READ-ONLY on the fly. Modifications can only be made off-line, by exact one process.

## When you want to update the dictionary:
*  generate new dictionary file offline;
*  copy the new file online, which has a different name with the old file;
*  modify configuration with the direction to the new file;
*  restart servers or processes one by one, double memory usage is needed;
*  remove the old file after restarting.
