FROM registry.gitlab.com/islandoftex/images/texlive:latest-basic
ARG TEXLIVE_VERSION=2023

RUN apt-get update && \
    apt-get install -y openssh-client && \
    # For svg importing
    apt-get install -y inkscape && \
    # For latexindent
    apt-get install -y libyaml-tiny-perl libfile-homedir-perl libunicode-linebreak-perl liblog-log4perl-perl libtest-log-dispatch-perl

# Add tex packages to path
ENV PATH ${PATH}:/usr/local/texlive/${TEXLIVE_VERSION}/bin/x86_64-linux:/usr/local/texlive/${TEXLIVE_VERSION}/bin/aarch64-linux

# Install packages
RUN tlmgr install latexmk chktex latexindent \
    datetime2 datetime2-english \
    svg koma-script trimspaces xcolor transparent pgf catchfile \
    glossaries && \
    texhash
