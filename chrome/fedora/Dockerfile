FROM docker.io/serverwentdown/env:fedora-desktopbase

RUN sudo dnf install -y \
		pulseaudio-libs \
		mesa-dri-drivers \
		mesa-libEGL \
		mesa-libGL \
	&& sudo dnf clean all \
	&& sudo rm -rf /var/cache/dnf

RUN sudo dnf install -y \
		dnf-plugins-core \
		# chromium-freeworld \
		# chromium-browser-privacy \
	&& sudo dnf config-manager --set-enabled google-chrome \
	&& sudo dnf install -y google-chrome-stable \
	&& sudo dnf clean all \
	&& sudo rm -rf /var/cache/dnf

#CMD ["/usr/bin/chromium-browser"]
CMD ["/usr/bin/google-chrome"]
