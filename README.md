# haproxy
Changing static-rr algo:  switch to next backend server only when we get 128 requests on previous server. 

Based on haproxy 1.7.10

Build method:

1. sudo apt install libssl-dev libpcre++-dev
2. make TARGET=linux2628 USE_PCRE=1 USE_OPENSSL=1 USE_ZLIB=1 USE_LIBCRYPT=1
3. replace /usr/sbin/haproxy and /usr/local/sbin/haproxy with new compiled haproxy executable.
4. service haproxy restart
