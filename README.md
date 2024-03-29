## Setting Up

1. **Create an environment file:**

   - Add the following line to the `.env` file, replacing `<WEBHOOK_ADDRESS>` with the actual URL you obtained from [https://webhook.site/](https://webhook.site/):

     ```plaintext
     REDIS_ADDRESS=redis:6379
     WEBHOOK_ADDRESS=<WEBHOOK_ADDRESS>
     ```

2. **Getting Started:**

   - Install the required Go packages using the command:
     ```bash
     go get .
     ```

3. **Build Docker Image and Run Containers:**

   - Build the Docker image and start the containers with the following command:
     ```bash
     docker-compose up -d --build
     ```

4. **Tracking Logs:**

   - Track the logs of your application and services using the command:
     ```bash
     docker-compose logs -f
     ```

## Testing

1. **Access the Application:**

   - Open your browser and navigate to [http://127.0.0.1:8000/payment](http://127.0.0.1:8000/payment).

2. **Check Logs:**

   - After accessing the payment endpoint, check the logs. If the implementation was successful, you should see a log entry similar to this in the console:
     ```plaintext
     api        | 192.168.65.1 - - [29/Mar/2024 15:38:33] "GET /payment HTTP/1.1" 200 -
     webhook-1  | 2024/03/29 15:38:34 delivered
     ```
