FROM docker.io/serverwentdown/env:fedora-desktopbase

RUN sudo dnf install -y \
		pulseaudio-libs \
		mesa-dri-drivers \
		mesa-libEGL \
		mesa-libGL \
	&& sudo dnf clean all \
	&& sudo rm -rf /var/cache/dnf

RUN sudo dnf install -y \
		pciutils-libs \
		ffmpeg-libs \
		firefox \
	&& sudo dnf clean all \
	&& sudo rm -rf /var/cache/dnf

ENV MOZ_ENABLE_WAYLAND=1
CMD ["/usr/bin/firefox"]
