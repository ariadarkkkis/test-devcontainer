FROM mcr.microsoft.com/devcontainers/dotnet:0-7.0-jammy

# Prevent 'Warning: apt-key output should not be parsed (stdout is not a terminal)'
ENV APT_KEY_DONT_WARN_ON_DANGEROUS_USAGE=1

# install NodeJS 18.x
RUN apt-get update -yq 
RUN apt-get install curl gnupg libgdiplus -yq 
RUN curl -sL https://deb.nodesource.com/setup_18.x | bash -
RUN apt-get install -y nodejs

# Install libgdiplus (DNTCaptcha fix)
RUN apt-get update -yq 
RUN apt-get install -yq
RUN cd /usr/lib
RUN ln -s libgdiplus.so gdiplus.dll
