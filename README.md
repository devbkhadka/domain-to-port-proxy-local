This is initial setup to map domain to port in local machine. This will
help us easily run different projects on local with different host names
which will be mapped to different port.

Steps:
- Lets say we have 3 projects A, B and C
- We can add domains and sub-domains related to those project on
`/etc/hosts` file
```
127.0.0.1 A.local api.A.local B.local api.B.local C.local
```
- Now we can map different ports to each in `domain_mapping.yaml` like
```
A.local 3000
api.A.local 8000
B.local 3001
api.B.local 8001
C.local 3002
```
- Setup project to serve on corresponding ports
- Start the mapper nginx server `docker-compose up -d`
- Now we can access our projects with respective domain and sub-domain names
