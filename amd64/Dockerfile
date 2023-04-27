FROM mysql:8.0.33-debian

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update; \
    apt install -y --no-install-recommends locales

RUN sed -i -e 's/# ko_KR.UTF-8 UTF-8/ko_KR.UTF-8 UTF-8/' /etc/locale.gen; \
    echo 'LANG="ko_KR.UTF-8"' >> /etc/default/locale; \
    dpkg-reconfigure --frontend=noninteractive locales; \
    update-locale LANG=ko_KR.UTF-8; \
    apt clean && rm -rf /var/lib/apt/lists/* /tmp/*

ENV LANG ko_KR.UTF-8
