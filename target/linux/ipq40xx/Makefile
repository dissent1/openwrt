include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=ipq40xx
BOARDNAME:=Qualcomm Atheros IPQ40XX
FEATURES:=squashfs fpu ramdisk nand
CPU_TYPE:=cortex-a7
CPU_SUBTYPE:=neon-vfpv4
MAINTAINER:=John Crispin <john@phrozen.org>

# TODO: drop kmod-usb-dwc3-of-simple when migrating to 4.19
KERNEL_PATCHVER:=4.14

KERNELNAME:=zImage Image dtbs

include $(INCLUDE_DIR)/target.mk
DEFAULT_PACKAGES += \
	kmod-usb-dwc3-of-simple \
	kmod-leds-gpio kmod-gpio-button-hotplug swconfig \
	kmod-ath10k-ct wpad-openssl \
	kmod-usb3 kmod-usb-dwc3 ath10k-firmware-qca4019-ct \
	block-mount e2fsprogs openssl-util luci luci-app-minidlna \
	luci-app-transmission transmission-daemon-openssl \
	kmod-usb-storage kmod-fs-ext4 minidlna nano htop rng-tools \
	aria2 luci-app-aria2 samba36-server luci-app-samba openssh-sftp-server

$(eval $(call BuildTarget))
