# SPDX-License-Identifier: GPL-3.0-or-later
# Copyright 2022, CZ.NIC z.s.p.o. (https://www.nic.cz/)

include $(TOPDIR)/rules.mk

PKG_NAME:=tiny-map-e
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/edenden/tiny-map-e.git
PKG_SOURCE_DATE:=2022-04-23
PKG_SOURCE_VERSION:=fc742e0278c63ef5acdc7e6f26e941d012bb6957
PKG_MIRROR_HASH:=d2d280d1a0c531f6e1fe20af49bafdbe61d42d573bcef4b11fd57cca2febca90

# TODO: add maintainer
PKG_LICENSE:=MIT

include $(INCLUDE_DIR)/package.mk

define Package/tiny-map-e
  SECTION:=net
  CATEGORY:=Network
  TITLE:=tiny-map-e
  URL:=https://github.com/edenden/tiny-map-e
  DEPENDS:=+kmod-tun
endef

define Package/tiny-map-e/description
  Tiny MAP-E implementation
  This implementation is based on draft-ietf-softwire-map-04.
endef

define Package/tiny-map-e/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(CP) $(PKG_BUILD_DIR)/map-e $(1)/usr/sbin
endef

$(eval $(call BuildPackage,tiny-map-e))
