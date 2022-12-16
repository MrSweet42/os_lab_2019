all: tcp udp

tcp: tcp_client tcp_server

tcp_client: tcpclient.c
	gcc -D SADDR='struct sockaddr' -D SIZE='sizeof(struct sockaddr_in)' tcpclient.c -o tcpclient

tcp_server: tcpserver.c
	gcc -D SADDR='struct sockaddr' tcpserver.c -o tcpserver

udp: udp_client udp_server

udp_client: udpclient.c
	gcc -D SADDR='struct sockaddr' -D SLEN='sizeof(struct sockaddr_in)' udpclient.c -o udpclient

udp_server: udpserver.c
	gcc -D SADDR='struct sockaddr' -D SLEN='sizeof(struct sockaddr_in)' udpserver.c -o udpserver

clean:
	rm * *.o -f