# Cache Implementation in Go

This repository contains a simple implementation of a cache using Go programming language. The cache is designed to store a fixed number of elements and evict the least recently used item when the cache is full.

## Code Explanation

The code consists of the following components:

### Node Struct
- `Node` represents a node in the cache. It contains a value (`Val`), a reference to the left node (`Left`), and a reference to the right node (`Right`).

### Queue Struct
- `Queue` represents a doubly linked list used to store the cache elements. It contains a reference to the head node (`Head`), a reference to the tail node (`Tail`), and the length of the queue (`Length`).

### Cache Struct
- `Cache` represents the cache data structure. It contains a `Queue` and a `Hash` map to store the elements.

### NewCache()
- `NewCache()` is a constructor function that creates and returns a new `Cache` instance with an empty queue and hash map.

### NewQueue()
- `NewQueue()` is a constructor function that creates and returns a new `Queue` instance with empty head and tail nodes.

### Check()
- `Check()` is a method of the `Cache` struct that checks if a given string (`str`) exists in the cache. If the string is found, the corresponding node is removed from the cache. If not found, a new node is created and added to the cache.

### Remove()
- `Remove()` is a method of the `Cache` struct that removes a given node (`n`) from the cache. It adjusts the references of the neighboring nodes and updates the cache length.

### Add()
- `Add()` is a method of the `Cache` struct that adds a given node (`n`) to the cache. It adjusts the references of the neighboring nodes, updates the cache length, and performs eviction if the cache size exceeds the predefined limit.

### Display()
- `Display()` is a method of the `Cache` struct that displays the current state of the cache. It prints the number of elements in the queue and the values of each node in the queue.

### Main Function
- The `main()` function demonstrates the usage of the cache by checking a list of words. It creates a new cache instance, checks each word, and displays the cache after each check.

## Usage

To use this cache implementation, follow these steps:

1. Clone the repository:

```
git clone <repository_url>
```

2. Navigate to the cloned directory:

```
cd <repository_directory>
```

3. Build and run the code:

```
go run main.go
```

4. Observe the output, which displays the cache state after each word check.

Feel free to modify the code and experiment with different scenarios to understand cache behavior.

## Conclusion

This cache implementation provides a basic understanding of how caching works in Go. It can be used as a starting point for more advanced cache implementations or integrated into other applications where caching is required.
