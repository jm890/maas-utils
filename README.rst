Updates hostnames in Maas from a source yaml file.

    --maas-url URL, -u URL      The HTTP url for Maas.  ie: http://127.0.0.1/MAAS
                                Can also be passed as an environment variable: MAAS_URL
    --api-key KEY, -k KEY       The API key for Maas. Can also be passed as an environment
                                variable: MAAS_API_KEY
    --version, -v               Version.
    --help, -h                  Hello.
    FILE                        YAML file containing hostname definitions.  See below for format.

    Both --maas-url and --api-key (or their env equivalent) are *required*.

    But if both environment variables and command line options are passed, the command line options
    take precedence.

    The YAML format consists of specifying the domain name, host name, and the "Power" IP address.
    The IP address is used to match the correct node in Maas.

    Example file
    ============

      example.com:
        node-01: 127.0.0.1
        node-02: 127.0.0.2

