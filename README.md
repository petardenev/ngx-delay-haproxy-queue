# ngx-delay-haproxy-queue
nginx 1.11.2 patched to work with ey-balancer and delay modules.


Included in the respository are:

EY-Balancer => https://github.com/ezmobius/nginx-ey-balancer

Nginx-Delay => https://github.com/perusio/nginx-delay-module

OpenSSL => https://github.com/openssl/openssl

setup is suitable for implementation of java microcaching  with low request responce answers min<100ms
ey-balancer patch done with posibility to use least_conn method on distributing the incoming requests to the backend
when a request is scheduled for distribution to the backend, its multiplied with the number of backend nodes and send-out to all of them using least_conn method,
then on return of first request responce, other 2 workers are killed, allowing more free network connection slots to the backend, but fast request responce answer.
