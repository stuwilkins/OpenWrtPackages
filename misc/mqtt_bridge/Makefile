include $(TOPDIR)/rules.mk

PKG_NAME:=mqtt_bridge
PKG_RELEASE:=1

PKG_LICENSE_FILES:=LICENSE
PKG_LICENSE:=MIT

PKG_SOURCE_URL:=https://github.com/stuwilkins/mqtt_bridge.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_DATE:=2018-12-25
PKG_SOURCE_VERSION:=c8bf658721cc046126b1cde2fc3cb2e5567c6a94

PKG_MAINTAINER:=Stuart B. Wilkins <stuwilkins@mac.com>

include $(INCLUDE_DIR)/package.mk

define Package/mqtt_bridge
	SECTION:=net
	CATEGORY:=Network
	TITLE:=MQTT Bridge for Thingsboard
	URL:=https://github.com/stuwilkins/mqtt_bridge
	DEPENDS:=+libpaho.mqtt.c +libconfig
endef

define Package/mqtt_bridge/description
	Forms a MQTT bridge between home automation and thingsboard
endef

define Package/mqtt_bridge/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/mqtt_bridge/mqtt_bridge $(1)/usr/bin
endef
	
$(eval $(call BuildPackage,mqtt_bridge))
