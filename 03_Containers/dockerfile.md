# Create your first Dockerfile

1. Create a directory: `mkdir <diectory-name>`
2. Inside the directory create an index.html file:
    ```html
    <h1>Welcome to my first docker-app</h1>
    
    ```
3. Inside the directory create following file: `Dockerfile` with Introduction for
creating a nginx-webserver which delivers the index.html file
4. Build your image `docker build -t webapp .`
5. Run your container based on your image
