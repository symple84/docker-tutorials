### **Docker Assignment: Getting Started with Images and Containers**

#### **Objective:**
Gain hands-on experience with Docker by pulling an image from Docker Hub, building a custom Docker image, running a container, and pushing the image back to Docker Hub.

---

### **Assignment Tasks**

#### **Task 1: Pull an Image from Docker Hub**
1. Use the `docker pull` command to download the official **nginx** image from Docker Hub.
2. Verify the image is available locally using the `docker images` command.
3. Run a container from the **nginx** image and expose it on port 8080 of your host.
4. Open a web browser and visit `http://localhost:8080` to confirm nginx is running.

---

#### **Task 2: Build a Custom Docker Image**
1. Create a directory named `custom-nginx`.
2. Inside the directory, create a `Dockerfile` with the following content:
   ```dockerfile
   FROM nginx:latest
   COPY index.html /usr/share/nginx/html/index.html
   ```
3. Add a custom `index.html` file to the same directory with personalized content (e.g., "Welcome to my custom nginx!").
4. Build a new Docker image with the command:
   ```bash
   docker build -t custom-nginx .
   ```
5. Verify the image is built using `docker images`.

---

#### **Task 3: Run a Container from the Custom Image**
1. Run a container using the newly built `custom-nginx` image and expose it on port 9090.
2. Open a web browser and visit `http://localhost:9090` to verify the custom nginx page is displayed.

---

#### **Task 4: Push the Image to Docker Hub**
1. Log in to Docker Hub using the `docker login` command.
2. Tag your custom image to match your Docker Hub repository:
   ```bash
   docker tag custom-nginx <your-dockerhub-username>/custom-nginx
   ```
3. Push the image to Docker Hub:
   ```bash
   docker push <your-dockerhub-username>/custom-nginx
   ```
4. Verify the image is successfully uploaded by checking your Docker Hub account.

---

### **Submission Requirements**
1. Screenshots of the following:
   - Pulling the **nginx** image.
   - Running the default nginx container.
   - Custom **index.html** file content displayed in a browser.
   - Docker Hub repository showing the pushed image.
2. Docker commands used for each task, listed step by step.

---

### **Evaluation Criteria**
- Proper execution of all commands and tasks.
- Successful creation and display of a custom web page.
- Correctly tagged and pushed image to Docker Hub.
- Clarity and completeness of screenshots and documentation.

This assignment combines basic Docker operations with hands-on practice to reinforce key concepts.
