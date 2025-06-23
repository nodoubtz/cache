# cache

A high-performance, easy-to-use caching library for efficient data storage and retrieval.

## Features

- Simple API for storing and retrieving data
- Supports multiple cache backends (e.g., in-memory, file, Redis)
- Configurable expiration and eviction policies
- Thread-safe operations
- Serialization support for complex objects
- Built-in cache statistics and monitoring

## Installation

```bash
# Using pip (if this is a Python project)
pip install cache
# Or clone this repository
git clone https://github.com/nodoubtz/cache.git
cd cache
```

> **Note:** Replace the installation command above with the appropriate one for your language (npm, composer, etc.) if not Python.

## Usage

```python
from cache import Cache

# Create a cache instance (in-memory)
cache = Cache()

# Set a value with optional expiration (in seconds)
cache.set("user_1", {"name": "Alice"}, expire=60)

# Retrieve a value
user = cache.get("user_1")
print(user)  # Output: {'name': 'Alice'}

# Delete a value
cache.delete("user_1")
```

### Advanced Usage

- **Switch to Redis backend:**
    ```python
    cache = Cache(backend="redis", host="localhost", port=6379)
    ```
- **Get cache statistics:**
    ```python
    stats = cache.stats()
    print(stats)
    ```

## Configuration

You can configure the cache using environment variables or constructor parameters:

- `CACHE_BACKEND`: `memory` (default), `redis`, `file`
- `CACHE_EXPIRE`: Default expiration time in seconds
- `CACHE_MAX_SIZE`: Maximum number of items to store

## Contributing

Contributions are welcome! Please open issues and pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

For questions or support, please open an [issue](https://github.com/nodoubtz/cache/issues).

---

> **Note:** Update code examples and installation instructions to match your library’s language and API if different from Python.
