# sysdig-examples

## Sysdig

1. Create directories.
    ```bash
    $ sudo mkdir -p /opt/sysdig/captures
    ```
1. Run a container for Sysdig.
    ```bash
    $ git clone https://github.com/wdstar/sysdig-examples.git
    $ cd sysdig-examples
    $ docker-compose up -d
    ```
1. Exec bash in the container and hit `sysdig` or `csysdig`.
    ```bash
    $ docker-compose exec sysdig bash
    root@32902614aff2:/# csysdig
    ```

## Sysdig Inspect

1. Capture by `sysdig`.
    ```bash
    $ sudo mkdir -p /opt/sysdig/captures
    $ sudo sysdig -w /opt/sysdig/captures/file.scap -M 10
    ```
1. Run Sysdig inspect on Docker.
    ```bash
    $ git clone https://github.com/wdstar/sysdig-examples.git
    $ cd sysdig-examples/inspect
    $ docker-compose up -d
    ```
1. Access http://localhost:3000/
1. Inspect `/captures/file.scap` on the Web UI.
