Nginx with ngx_http_proxy_connect_module and quic-http/3 (openssl)

Curl with http/3 (quiche-boringssl)

/nginx/Dockerfile.build - just build and run

/nginx/Dockerfile.builddeb - make deb, install and run

/curl/Dockerfile - just build and run 

    CURL 8.7.1 QUICHE 0.20.1 :
    alpine:3.16 version: docker pull runalsh/curl:alpine (43MB)
    debian:12-slim version: docker pull runalsh/curl:latest (134MB)

    docker run --rm runalsh/curl curl --version
    docker run --rm runalsh/curl curl -sIL https://blog.cloudflare.com --http3 -H 'user-agent: mozilla' | grep 'HTTP/3'    
    docker run --rm runalsh/curl curl -sIL https://httpbin.org/brotli | grep -i 'content-encoding: br'
    docker run --rm runalsh/curl curl -sIL https://httpbin.org/gzip | grep -i 'content-encoding: gzip'
    docker run --rm runalsh/curl curl -sIL https://httpbin.org/get | grep -i 'HTTP/2'
