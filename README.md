# Simple Rust TCP Server

This is a simple TCP server implemented in Rust that serves HTTP requests. It listens on `127.0.0.1:7878` and responds with either the content of `index.html` or `404.html` based on the request received.

## Prerequisites

Before running the server, ensure you have Rust installed on your system. If not, you can install it from [rust-lang.org](https://www.rust-lang.org/tools/install).

## Usage

1. Clone the repository:

    ```bash
    git clone https://github.com/0xSaksham/single-thread-server.git
    ```

2. Navigate into the project directory:

    ```bash
    cd single-thread-server
    ```

3. Compile and run the server:

    ```bash
    cargo run
    ```

4. Open your web browser and visit `http://127.0.0.1:7878` to see the server in action.

## Structure

- `src/main.rs`: Contains the main server implementation.
- `index.html`: Sample HTML file served when the request is `GET /`.
- `404.html`: Sample HTML file served when the request is not `GET /`.

## How It Works

The server listens on `127.0.0.1:7878` for incoming TCP connections. Upon receiving a connection, it reads the request line to determine the requested resource (`index.html` or `404.html`). Then, it reads the corresponding file, constructs an HTTP response, and sends it back to the client.

## Customization

Feel free to modify `index.html` and `404.html` to serve your own content. You can also extend the server to handle different types of requests or add more features as needed.

---