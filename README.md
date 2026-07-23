<div align="center">
  <a href="https://github.com/lukas-sgx/">
    <img src="https://github.com/OpenCz/McpDesk/blob/main/assets/logo.svg?raw=true" alt="Logo" height="180" style="border-radius: 10px">
  </a>

  <h3 align="center">McpDesk</h3>

  [![Crates.io version](https://img.shields.io/crates/v/mcpserver-sdk?style=for-the-badge)](https://crates.io/crates/mcpserver-sdk)
  [![Build Status](https://img.shields.io/github/actions/workflow/status/OpenCz/McpDesk/ci.yml?style=for-the-badge)](https://github.com/OpenCz/McpDesk/actions)

  <p align="center">
    A Software Development Kit for developers who want to build MCP Servers in Rust.
    <br />
    <a href="https://github.com/OpenCz/McpDesk/tree/main/docs"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/OpenCz/McpDesk">View Demo</a>
    &middot;
    <a href="https://github.com/OpenCz/McpDesk/issues/new?template=bug-report.yml">Report Bug</a>
    &middot;
    <a href="https://github.com/OpenCz/McpDesk/issues/new?template=feature-request.yml">Request Feature</a>
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## About The Project

This SDK aims to simplify the creation of MCP (Model Context Protocol) servers by allowing developers to write them entirely in Rust, with a simple CLI for scaffolding, validation, and running servers.

### Built With

[![Rust][Rust-shield]][Rust-url]

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

You need a recent Rust toolchain (via `rustup`) installed on your system.

### Installation

#### Development mode (clone the repo, with local changes)
1. Clone the repo
```sh
git clone https://github.com/OpenCz/McpDesk.git
cd McpDesk
```
2. Build the SDK locally
```sh
cargo build
```

#### Release mode (stable version from crates.io)
```sh
cargo add mcpserver-sdk
```

## Usage

Here is a quick example of how to scaffold and inspect a new MCP server:
```sh
$ mcpserver-sdk new my-server
Creating project 'my-server'...
|-- server
|   |-- name: my-server
|   `-- transport: stdio
|-- manifest:
|   |-- valid: True
|   `-- schema_version: 2025-06
|-- tools:
|   |-- count: 0
|   `-- status: none registered
|-- resources:
|   |-- count: 0
|   `-- status: none registered
`-- build:
    |-- target: release
    `-- status: ready
```

*For more advanced examples, please refer to the [Documentation](https://github.com/OpenCz/McpDesk/tree/main/docs).*

## Roadmap

- [ ] Automated manifest validator for MCP servers
- [ ] Automated compilation to a distributable binary
- [ ] Project scaffolding pipeline (`new`, `build`, `run`)
- [ ] Core MCP bindings (Tools, Resources, Prompts)
- [ ] Transport adapters (stdio, SSE, streamable HTTP)

See the [open issues](https://github.com/OpenCz/McpDesk/issues) for a full list of proposed features (and known issues), and [CHANGELOG.md](./CHANGELOG.md) for release history.

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for setup instructions, commit conventions, and the PR process.

### Top contributors:

<a href="https://github.com/OpenCz/McpDesk/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenCz/McpDesk" alt="contrib.rocks image" />
</a>

## License

Distributed under the MIT License. See [LICENSE](./LICENSE) for more information.

## Contact

@Lukas-sgx
@Celz-Pch

## Acknowledgments

* [Model Context Protocol Spec](https://modelcontextprotocol.io/) - Official MCP specification
* [rust-sdk](https://github.com/modelcontextprotocol/rust-sdk) - Reference Rust implementation

[Rust-shield]: https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white
[Rust-url]: https://www.rust-lang.org/