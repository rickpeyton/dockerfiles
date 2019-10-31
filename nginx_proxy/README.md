# nginx_proxy

The included Dockerfile builds off of the official nginx Docker image, installs openssl, creates a self-signed certificate, and overwrites the default nginx.conf with the nginx.conf in this repo.

The modified nginx.conf references the self-signed cert and key, answers all traffic on port 443 and forwards that traffic to port 3000 via http://host.docker.internal.

When running the image forward 443 to 443

`docker run -it --rm -p 443:443 ...`
