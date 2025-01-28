# SocketSaga

SocketSaga is a Java-based project demonstrating different implementations of socket programming patterns, from basic single-threaded connections to advanced thread pool management. This project serves as an educational resource for understanding network programming and concurrent server architectures in Java.

## Project Structure

The project contains three main implementations:

1. **Single-Threaded Implementation**
   - Basic client-server communication
   - One connection handled at a time
   - Located in the `singlethreaded` package

2. **Multi-Threaded Implementation**
   - Handles multiple clients simultaneously
   - Creates a new thread for each connection
   - Uses Java's functional interfaces
   - Located in the `multithreaded` package

3. **Thread Pool Implementation**
   - Efficient handling of multiple clients using a thread pool
   - Prevents thread explosion under high load
   - Configurable pool size
   - Located in the `threadpool` package

## Features

- Multiple socket programming patterns demonstrated
- Configurable server ports and timeouts
- Error handling and resource management
- Client-side connection pooling
- Server-side connection acceptance
- Bidirectional communication

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- Java IDE (recommended: IntelliJ IDEA or Eclipse)

### Running the Applications

#### Single-Threaded Version
1. Start the server:
```bash
javac singlethreaded/Server.java
java singlethreaded.Server
```

2. Start the client:
```bash
javac singlethreaded/Client.java
java singlethreaded.Client
```

#### Multi-Threaded Version
1. Start the server:
```bash
javac multithreaded/Server.java
java multithreaded.Server
```

2. Start the client:
```bash
javac multithreaded/Client.java
java multithreaded.Client
```

#### Thread Pool Version
1. Start the server:
```bash
javac threadpool/Server.java
java threadpool.Server
```

## Implementation Details

### Single-Threaded Server
- Basic implementation using `ServerSocket`
- Handles one client at a time
- Includes timeout configuration
- Suitable for learning basic socket programming concepts

### Multi-Threaded Server
- Uses Java's Thread class for concurrent client handling
- Implements functional interfaces for client processing
- Lambda expressions for cleaner code
- Creates a new thread per client connection

### Thread Pool Server
- Uses `ExecutorService` for efficient thread management
- Configurable thread pool size
- Better resource utilization
- Prevents thread explosion under high load

## Technical Considerations

- All implementations use port 8010 by default
- Servers include timeout configurations
- Proper resource cleanup with try-with-resources
- Error handling for network operations

## Contributing

Feel free to submit issues and enhancement requests. Follow these steps to contribute:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the GNU v3.0 License - see the LICENSE file for details.

## Acknowledgments

- This project serves as an educational resource for learning socket programming in Java
- Demonstrates the evolution of server implementations from basic to advanced patterns
- Showcases best practices in Java network programming
