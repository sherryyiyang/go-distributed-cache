# go-distributed-cache

A lightweight, in-memory distributed caching system implemented in Go, designed for scalability and simplicity.


## Features
**In-Memory Caching**: Fast data retrieval using Go's native data structures.

**Distributed Architecture**: Supports multiple nodes to share and manage cache data.

**Consistent Hashing**: Efficiently distributes keys across nodes to balance load and ensure scalability.

**HTTP-Based Communication**: Nodes communicate over HTTP, facilitating easy integration and deployment.

**LRU Eviction Policy**: Implements Least Recently Used strategy to manage cache size and evict stale entries.
GitHub

## Getting Started
Prerequisites
Go 1.16 or higher

Installation
Clone the repository:
```
git clone https://github.com/sherryyiyang/go-distributed-cache.git
cd go-distributed-cache
Build the project:
```

```
go build -o cache
Run the cache server:
```

```
./cache -port=8001 -peers=http://localhost:8001,http://localhost:8002,http://localhost:8003
Repeat the above step with different ports (e.g., 8002, 8003) to simulate multiple nodes.
```

## Usage
The cache server exposes the following HTTP endpoints:

GET /cache/{key}: Retrieve the value associated with the specified key.

POST /cache: Add a new key-value pair to the cache. The request body should be a JSON object:


## Testing
Run the unit tests using the following command:

bash
Copy
Edit
go test ./...
Project Structure
