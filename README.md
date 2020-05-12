# sysdig-examples

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
1. Access http://localhost:8080/
1. Inspect `/captures/file.scap` on the Web UI.
