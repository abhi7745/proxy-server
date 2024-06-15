# ngrok

## Introduction
ngrok is a tool that creates secure tunnels to your localhost, making your local server accessible over the internet. This is useful for testing webhooks, demoing websites, and more.

## Prerequisites
- An ngrok account (sign up at https://ngrok.com/)
- ngrok binary (download from https://ngrok.com/download)

## Setup

1. **Download and Install ngrok:**

    - For Windows:
      Download the zip file from the ngrok website and extract it. Add the ngrok executable to your PATH.

2. **Authenticate ngrok:**
    ```bash
    ngrok config add-authtoken YOUR_AUTH_TOKEN
    ```
    Replace `YOUR_AUTH_TOKEN` with the authentication token from your ngrok dashboard.

## Running ngrok

1. **Expose a local web server:**

    ```bash
    ngrok http 80
    ```
    This command tells ngrok to create a tunnel to your local web server running on port 80. The output will include a public URL that you can use to access your local server from the internet.

2. **Specify a different port:**

    ```bash
    ngrok http 3000
    ```
    Replace `3000` with the port number your application is running on.

2. **Static free domain by ngrok:**
    ```bash
    ngrok http --domain=<your-free-domain-by-ngrok>.ngrok-free.app 80
    ```

4. **Expose a TCP port:**

    ```bash
    ngrok tcp 22
    ```
    This command creates a TCP tunnel to port 22, typically used for SSH.

## Advanced Usage

1. **Custom Subdomains and Domains:**
   - To use custom subdomains:
     ```bash
     ngrok http -subdomain=myapp 80
     ```
     Replace `myapp` with your desired subdomain (requires a paid plan).

   - To use custom domains:
     ```bash
     ngrok http -hostname=mycustomdomain.com 80
     ```
     Replace `mycustomdomain.com` with your domain (requires DNS configuration and a paid plan).

2. **Inspect Traffic:**
   - ngrok provides a web interface to inspect traffic:
     ```bash
     http://localhost:4040
     ```

## Stopping ngrok

To stop the ngrok tunnel, simply press `CTRL+C` in the terminal where ngrok is running.

## Conclusion

ngrok is a powerful tool for exposing local servers to the internet. With the basic setup and commands provided above, you can easily start using ngrok for various development and testing scenarios.

For more details and advanced configurations, refer to the [ngrok documentation](https://ngrok.com/docs).
