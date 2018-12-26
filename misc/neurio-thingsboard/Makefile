include $(TOPDIR)/rules.mk

PKG_NAME:=neurio-thingsboard
PKG_RELEASE:=1

PKG_LICENSE_FILES:=LICENSE
PKG_LICENSE:=MIT

PKG_SOURCE_URL:=https://github.com/stuwilkins/neurio-thingsboard.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_DATE:=2018-12-25
PKG_SOURCE_VERSION:=8f084dccbe6a0d04488330732e0be72ee5bf89fe

PKG_MAINTAINER:=Stuart B. Wilkins <stuwilkins@mac.com>

include $(INCLUDE_DIR)/package.mk

define Package/neurio-thingsboard
	SECTION:=net
	CATEGORY:=Network
	TITLE:=Neurio Bridge for Thingsboard
	URL:=https://github.com/stuwilkins/neurio-thingsboard
	DEPENDS:=+libpaho.mqtt.c +curl +libjson-c 
endef

define Package/neurio-thingsboard/description
	Forms a MQTT bridge between the neurio home energy monitor and thingsboard
endef

define Package/neurio-thingsboard/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/bin/neurio-thingsboard $(1)/usr/bin
endef
	
$(eval $(call BuildPackage,neurio-thingsboard))
