FROM rust:1.75-buster

RUN apt-get update && \
    apt-get -y install git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rustup update && \
    rustup component add rls rust-analysis rust-src rustfmt clippy && \
    rustup toolchain install nightly --component rust-analyzer-preview && \
    cargo install cargo-edit cargo-watch

ENV CARGO_BUILD_TARGET_DIR=/tmp/target

WORKDIR /app
