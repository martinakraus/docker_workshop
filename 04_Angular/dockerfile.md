# Create your first Dockerfile

1. Create a new Angular Application `ng new ng-docker`
2. Inside the directory create following file: `Dockerfile` 
3. Define Instruction for building the image
   * Base Image? Search on Dockerhub
   * Define working directory: `WORKDIR /app`
   * Which file needs to be copied for an Angular Application to be build? `COPY package*.json /app/`
   * Build: `RUN npm ci`
   * Which other files need to be copied inside the container for the app to run?
   ```bash
    COPY angular.json /app/angular.json
    COPY ts*.json /app/
    COPY ./src /app/src
    ```
   * And finally run it and expose Port 4200: `RUN npm start`
   
4. Build your image `docker build -t webapp .`
5. Run your container based on your image
