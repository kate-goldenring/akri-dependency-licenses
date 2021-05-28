# Akri Dependency Licenses Tool
This project consists of several dockerfiles for outputting the licenses of all of Akri dependencies.
[Akri](https://github.com/deislabs/akri) is an OSS IoT and Kubernetes project that consists of Rust, 
Python, and .NET Core components.
While there are tools such as the [OSS Review Toolkit](https://github.com/oss-review-toolkit/ort) 
that are availabile for checking the 
licenses of OSS dependencies, their versatility make for complicated usage scenarios.

This project consists of a Dockerfiles that, when built, output a list of Akri's dependencies and their licenses. 
There is a separate Dockerfile for each language.
The following tools were used for each of the languages:
| Language      | Tool |
| ----------- | ----------- |
| Rust  | [cargo-license](https://github.com/onur/cargo-license) |
| .NET Core   | [dotnet-delice](https://github.com/aaronpowell/dotnet-delice) |
| Python   | [pip-licenses](https://pypi.org/project/pip-licenses/) |

## Usage
1. Clone and navigate to the root of the repository
    ```sh
    https://github.com/kate-goldenring/akri-dependency-licenses.git
    cd akri-dependency-licenses
    ```
1. Output licenses of Akri's Rust dependencies
    ```sh
    sudo docker build --no-cache -f ./Dockerfile.rust-deps  .
    ```
1. Output licenses of Akri's .NET Core dependencies
    ```sh
    sudo docker build --no-cache -f ./Dockerfile.dotnet-deps  .
    ```
1. Output licenses of Akri's Python dependencies
    ```sh
    sudo docker build --no-cache -f ./Dockerfile.python-deps  .
    ```


