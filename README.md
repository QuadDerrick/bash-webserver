A web server serving a single character (.) with log functionality.

EVERYONE says you its a bad idea to run a web server with nc NOBODY tells you why, beyond the obvious, its a security risk. ALL services is a security risk.

To have a unpriviledged user recieve web traffic at port 80(http) rerouting it localy. Run as root :

iptables -A PREROUTING -t nat -p tcp --dport 80 -j REDIRECT --to-ports 4616
