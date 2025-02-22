# Install RabbitMQ on Ubuntu

1. First things first.
   
   ```sh
      sudo apt update && sudo apt upgrade -y
   ```

3. Install Erlang.

   ```sh
   sudo apt install -y erlang
   ```

4. Add the correct RabbitMQ repository.

  ```sh
  echo "deb https://packages.rabbitmq.com/debian/ erlang-23.x main" | sudo tee -a /etc/apt/sources.list.d/rabbitmq.list
  ```

5. Download the RabbitMQ signing key.
   
  ```sh
   wget -qO - https://packages.rabbitmq.com/rabbitmq-signing-key-public.asc | sudo tee /etc/apt/trusted.gpg.d/rabbitmq.asc
   ```
6. Update your system.

   ```sh
   sudo apt update
   ```

7. Install RabbitMQ.

   ```sh
   sudo apt install rabbitmq-server -y
   ```

8. Start RabbitMQ.

   ```sh
   sudo systemctl start rabbitmq-server
   ```

9. Verify the status of RabbitMQ Server.
    
   ```sh
   sudo systemctl status rabbitmq-server
   ```
