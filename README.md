# Flam_assignment

**LRU Cache Implementation**
This project is about implementing an LRU (Least Recently Used) Cache. The main goal was to make get and put operations work in constant time — O(1).

How it works
I used a combination of a hash map and a doubly linked list:
The hash map stores the key and a pointer to the corresponding node in the list.
The list keeps track of the order in which keys are used.
The most recently used item is kept at the front.
The least recently used one is at the back, so it's easy to remove when the cache is full.

Operations
get(key):
If the key is present, it returns the value and moves that key to the front (because it was recently used). If not present, it returns -1.

put(key, value):
If the key already exists, it updates the value and moves it to the front.
If the key is new and the cache is full, it removes the least recently used key (from the back) and inserts the new one at the front.



 **Implementation of simplified version of a HashMap**
This is a simple C++ implementation of a HashMap (like a dictionary) without using any built-in hash table or map. I used an array and linked list to store key-value pairs.

What It Does
put(key, value) → Adds or updates a key with a value.
get(key) → Returns the value if the key exists, otherwise returns -1.
remove(key) → Deletes the key and its value from the map.

How It Works
I used an array of fixed size (a prime number) and a hash function to place keys in different "buckets". Each bucket uses a linked list to handle multiple keys in case of collisions.

