FROM debian:bookworm-slim

RUN set -ex \
    && echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
	build-essential \
        devscripts \
	fakeroot \
	debhelper \
	dh-autoreconf \
    && apt-get -y autoremove \
    && apt-get clean \
    && rm -rf /tmp/* /var/tmp/* /var/log/* /var/lib/apt/lists/* /var/log/alternatives.log

RUN chmod a+rwx,u+t /tmp

ENTRYPOINT []
CMD ["/bin/sh"]
