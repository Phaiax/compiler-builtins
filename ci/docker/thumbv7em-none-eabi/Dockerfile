FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y --no-install-recommends \
    ca-certificates curl gcc gcc-arm-none-eabi libc6-dev libcurl4-openssl-dev libssh2-1 libnewlib-dev
RUN curl -sf "https://raw.githubusercontent.com/japaric/rust-everywhere/master/install.sh" | \
    bash -s -- --at /usr/bin --from japaric/xargo --for x86_64-unknown-linux-gnu --tag v0.1.13
ENV AR_thumbv7em_none_eabi=arm-none-eabi-ar \
    CARGO_TARGET_THUMBV7EM_NONE_EABI_LINKER=arm-none-eabi-gcc \
    CC_thumbv7em_none_eabi=arm-none-eabi-gcc \
