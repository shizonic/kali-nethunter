# Defaults
DEVICE=angler
ANDROID_VERSION=marshmallow
FORCE_DOWN=--forcedown

# Make all (Release, Release without rootfs, Kernel ony, Uninstaller)
all:
	make clean
	make DEVICE=angler release release-no-rootfs kernel uninstaller
	make DEVICE=bullhead release release-no-rootfs kernel uninstaller

# Release
release:
	python build.py --device $(DEVICE) --$(ANDROID_VERSION) --rootfs full $(FORCE_DOWN) --release v3.0

# Release without rootfs
release-no-rootfs:
	python build.py --device $(DEVICE) --$(ANDROID_VERSION) $(FORCE_DOWN) --release v3.0

# Kernel only
kernel:
	python build.py --device $(DEVICE) --$(ANDROID_VERSION) --kernel $(FORCE_DOWN)

# Uninstaller
uninstaller:
	python build.py --uninstaller

# Cleaner
clean:
	rm -f kernel-nethunter-*.zip nethunter-*.zip uninstaller-nethunter-*.zip update-nethunter-*.zip
