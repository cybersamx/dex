# Dex Notes

## Setup

### Configuration

Edit `examples/config-dev.yaml` to configure the application.

### Run the application

1. Run dex server.

   ```shell
   mkdir bin
   cd cmd/dex
   go build -v -ldflags -w -o ../../bin/dex .
   cd ../..
   bin/dex serve examples/config-dev.yaml
   ```

1. Launch another shell and run dex web client.

   ```shell
   cd examples/example-app
   go build -v -o ../../bin/dex-client .
   cd ../..
   bin/dex-client
   ```

1. Launch a web browser and navigate to <http://localhost:5555>.
1. On the website, click the **Login** button.
1. On the next page, click **Log in with Example** button.
