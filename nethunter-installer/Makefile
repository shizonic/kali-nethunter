# Make all (Release, Release without rootfs, Kernel ony, Uninstaller)
all: clean release release-no-rootfs kernel uninstaller

# Release
release:
	python build.py --device angler --marshmallow --rootfs full --release v3.0

# Release without rootfs
release-no-rootfs:
	python build.py --device angler --marshmallow --release v3.0

# Kernel only
kernel:
	python build.py --device angler --marshmallow --kernel

# Uninstaller
uninstaller:
	python build.py --uninstaller

# Cleaner
clean:
	rm -f kernel-nethunter-angler-*.zip nethunter-angler-*.zip uninstaller-nethunter-*.zip update-nethunter-angler-*.zip
