# Node.js Docker Example

This project demonstrates how to containerize a simple Node.js application using Docker.

## Project Structure

```
.
├── Dockerfile
├── index.js
├── package.json
├── .dockerignore
```

## Files

- **Dockerfile**: Instructions to build the Docker image.
- **index.js**: Main Node.js application file.
- **package.json**: Project dependencies and metadata.
- **.dockerignore**: Prevents `node_modules` from being copied into the image.

## How to Build and Run

1. **Build the Docker image:**
   ```sh
   docker build -t myapp .
   ```

2. **Run the Docker container:**
   ```sh
   docker run -p 3000:9000 myapp
   ```
   This maps port 9000 inside the container to port 3000 on your host.

## Notes

- The application listens on port 9000 inside the container.
- The `.dockerignore` file ensures `node_modules` is not copied into the image, keeping it clean and reducing build size.

## License

This project is for