FROM docker.io/serverwentdown/env:alpine-desktopbase

RUN sudo apk add --no-cache \
		libpulse \
		mesa-dri-intel \
		mesa-dri-nouveau \
		mesa-egl \
		mesa-gl

RUN sudo apk add --no-cache \
		pciutils-libs \
		ffmpeg-libs \
		firefox

ENV MOZ_ENABLE_WAYLAND=1
CMD ["/usr/bin/firefox"]
