include $(TOPDIR)/rules.mk

PKG_NAME:=tiny-map-e
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/edenden/tiny-map-e.git
PKG_SOURCE_DATE:=2013-02-12
PKG_SOURCE_VERSION:=78962f952c9a4cf75707ce651548dda50e9d6e92
PKG_MIRROR_HASH:=7bc0e3b5bec4857eefbd5b83d408f329942145837f6dea86195739aead7d7f9e

# TODO: add maintainer and license

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
