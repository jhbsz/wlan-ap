include $(TOPDIR)/rules.mk

ARCH:=aarch64
BOARD:=ipq807x
BOARDNAME:=Qualcomm Atheros IPQ807x
FEATURES:=ubifs squashfs fpu ramdisk nand pcie usbgadget
CPU_TYPE:=cortex-a53
CPU_SUBTYPE:=neon-vfpv4
MAINTAINER:=John Crispin <blogic@openwrt.org>
SUBTARGETS:=generic ipq807x_32

KERNELNAME:=zImage Image dtbs

KERNEL_PATCHVER:=5.4
KERNEL_NAME_SUFFIX=-qsdk-26349818b464f8c7b52d59ce73579d9f3dd6bd5d

GENERIC_BACKPORT_DIR :=
GENERIC_PATCH_DIR :=
GENERIC_HACK_DIR :=
GENERIC_FILES_DIR := 
GENERIC_LINUX_CONFIG:=${CURDIR}/config-$(KERNEL_PATCHVER)-qsdk

include $(INCLUDE_DIR)/target.mk
DEFAULT_PACKAGES += kmod-qca-nss-dp kmod-qca-ssdk swconfig \
	kmod-qca-nss-drv qca-nss-fw-ipq807x \
	kmod-usb-phy-ipq807x kmod-usb-dwc3-qcom-internal \
	kmod-ath11k-ahb ath11k-firmware-ipq807x \
	kmod-gpio-button-hotplug iwinfo \
	qca-ssdk-shell kmod-bootconfig \
	uboot-envtools -procd-ujail

$(eval $(call BuildTarget))
