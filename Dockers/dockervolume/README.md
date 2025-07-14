# React + Vite App with Docker Volume

This project is a simple React app (created with Vite) that demonstrates how to use Docker volumes to share code between your Windows host and a Docker container.

## How to Use

1. **Build your React app locally** (optional for development):

   ```sh
   npm install
   npm run dev
   ```

2. **Run a Docker container with a volume mount:**

   ```sh
   docker run -it -v "C:\Users\varun\Desktop\Dev\DevOps\Dockers\dockervolume:/data" node bash
   ```

   - This mounts your local `dockervolume` folder to `/data` inside the container.

3. **Access your code inside the container:**

   ```sh
   cd /data
   ls
   ```

   You should see your React app files (like `src/App.jsx`).

## Why Use Docker Volumes?

- **Live development:** Edit files on your host and see changes in the container.
- **Persistence:** Files remain even if the container is removed.
- **Separation:** Keeps your development environment isolated.

## Example: Editing the App

Open `src/App.jsx` and change the text:

```jsx
<p>
  Edit <code>src/App.jsx</code> and save to test HMR
</p>
```

Save the file and see your changes reflected in the running app (if using a dev server).

---

**Learn more:**  
- [Docker Volumes](https://docs.docker.com/storage/volumes/)
- [Vite](https://vitejs.dev/)