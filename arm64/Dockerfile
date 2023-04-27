FROM mysql:8.0.33-oracle

RUN microdnf install -y glibc-locale-source glibc-langpack-en; \
	localedef -c -i ko_KR -f UTF-8 ko_KR.UTF-8; \
	localectl set-locale LANG=ko_KR.UTF-8; \
	microdnf clean all

ENV LANG=ko_KR.UTF-8
