# The Differences between HTTP 1.1 vs HTTP 2
## HTTP 1.1
### 1. **Single Request-Response Paradigm**
   - HTTP 1.1 operates on a request-response model, meaning that for each resource (like an image, stylesheet, or script), a separate connection needs to be established.

### 2. **Head of Line Blocking**
   - One of the notable drawbacks of HTTP 1.1 is head-of-line blocking. If a resource is slow to load, it can prevent other resources from loading, even if they could have been fetched in parallel.

### 3. **Multiple Connections**
   - To load a webpage, a browser typically opens multiple connections to the server. This process can be resource-intensive and slow, especially for mobile devices or slower internet connections.

### 4. **No Server Push**
   - In HTTP 1.1, the server can't push resources to the client. The client must explicitly request each resource, which can result in suboptimal performance.

### 5. **Compression is Optional**
   - While HTTP 1.1 supports content compression (gzip or deflate), it's optional. This means that servers might not always compress their responses, leading to larger payloads.

## HTTP 2

### 1. **Multiplexing**
   - Perhaps the most significant improvement in HTTP 2 is multiplexing. It allows multiple requests and responses to be sent and received on a single connection simultaneously. This eliminates the head-of-line blocking problem.

### 2. **Binary Framing Layer**
   - HTTP 2 uses a binary framing layer, which makes it more efficient in parsing and transmitting data. This is a departure from the plain text format of HTTP 1.1.

### 3. **Server Push**
   - HTTP 2 allows servers to proactively send resources to the client before they are explicitly requested. This can greatly reduce the number of round trips needed to load a webpage.

### 4. **Header Compression**
   - In HTTP 2, headers are compressed, reducing the overhead associated with sending a request. This is a significant improvement over HTTP 1.1, where headers are sent in plain text.

### 5. **One Connection per Origin**
   - HTTP 2 encourages the use of a single connection for all resources from the same origin. This reduces the overhead of establishing and maintaining multiple connections.

#