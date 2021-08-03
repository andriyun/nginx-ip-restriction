# NGINX restriction in action.

Example on Nginx restriction configuration. See `default.conf`

URL's allowed only from host machine and container nginx_restriction_vm1:
http://10.10.10.5
http://10.10.10.5/intern
http://10.10.10.5/intern/test.html

URL's allowed only from every where:
http://10.10.10.5/extern
http://10.10.10.5/extern/test.html


URL's NOT allowed from nginx_restriction_test:
http://10.10.10.5
http://10.10.10.5/intern
http://10.10.10.5/intern/test.html


1. Run docker-compose up

2. Open browser and check URL's from host machine

3. Get console access and vm1 from nginx_restriction_vm1 `docker exec -it nginx_restriction_vm1 bash`.
you need to install curl first `apt update && apt install curl -y`

4. Get console access and test from nginx_restriction_test `docker exec -it nginx_restriction_test bash`
