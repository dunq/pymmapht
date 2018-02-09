# pymmapht
* A mmap hashtable in python, with compact space use.
* Derived from [pyshmht](https://github.com/felix021/pyshmht.git).
* Can be useful for python http servers, e.g. tornado, and data processing with multiple processes.
* Limititaions: READ-ONLY on the fly. Modifications can only be made off-line, by exact one process.

## When you want to update the dictionary:
1. Generate new dictionary file offline.
2. Copy the new file online, which has a different name from the old file.
3. Modify configuration to use the new file.
4. Restart servers or processes one by one, where double memory usage is needed.
5. Remove the old file after the restarting.
