
# Pimcore extended image
This repository contains a Docker image configured for various development and production purposes. The image is based on PHP 8.0 and includes a variety of useful extensions and tools.

## Included Extensions and Tools

- **Supervisor**: Process control system to manage multiple processes within a container.
- **Locales**: Support for various locales and localizations.
- **Unzip**: Utility for unpacking ZIP files.
- **Development Packages**:
    - `zlib1g-dev`
    - `libpng-dev`
    - `libjpeg-dev`
    - `libbz2-dev`
    - `libicu-dev`
    - `libzip-dev`
- **Compression Tools**: `zip`
- **Fonts**: `fonts-roboto`
- **SSH Server**: `openssh-server`
- **Sudo**: `sudo`
- **Supervisor**: Already mentioned, but included again to ensure functionality.
- **SSH Libraries**:
    - `libssh2-1`
    - `libssh2-1-dev`
- **Timezone Data**: `tzdata`
- **Scheduled Tasks**: `cron`
- **System Logging**: `rsyslog`
- **Editor**: `vim`
- **Image Processing**:
    - `libmagick++-dev`
    - `imagemagick`
    - `inkscape`
- **Video and Audio Processing**: `ffmpeg`

## Prerequisites

- Docker must be installed on your system. You can download and install Docker [here](https://www.docker.com/products/docker-desktop).

## Installation

1. Clone this repository to your local system:
    ```bash
    git clone https://github.com/etarkhan/pimcore-extended.git
    cd https://github.com/etarkhan/pimcore-extended.git
    ```

2. Build the Docker image:
    ```bash
    docker build -t docker-extended .
    ```

## Usage

You can start the container with the following command:

```bash
docker run -d -p 80:80 docker-extended
```

## Known Issues

Document any known issues and their solutions here. If there are none, leave this section blank or remove it.

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request with your changes. We appreciate all feedback and improvements!

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

If you have any questions or suggestions, feel free to contact us:

- Your Name: Aref Tarkhani
- Email: aref.tarkhani@gmail.com

---
