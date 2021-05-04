FROM docker.io/serverwentdown/env:fedora-desktopbase

RUN sudo dnf install -y \
		pulseaudio-libs \
		mesa-dri-drivers \
		mesa-libEGL \
		mesa-libGL \
	&& sudo dnf clean all \
	&& sudo rm -rf /var/cache/dnf

RUN sudo dnf install -y \
		chromium-freeworld \
		# chromium-browser-privacy \
	&& sudo dnf clean all \
	&& sudo rm -rf /var/cache/dnf

CMD ["/usr/bin/chromium-browser"]
