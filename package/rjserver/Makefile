#
# Copyright (C) 2006-2011 Xmlad.com
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=rjserver
PKG_VERSION:=1.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
#PKG_SOURCE_URL:=http://mentohust.googlecode.com/files/
#PKG_MD5SUM:=c7033ba8d8e75294924ed03f4b7b0c45

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/rjserver
	SECTION:=net
	CATEGORY:=Network
	DEPENDS:=+libpcap
	TITLE:=An fake ruijie server
	URL:=https://github.com/morfast/ruijie-server
	SUBMENU:=CERNET
endef

define Build/Prepare
	$(call Build/Prepare/Default)
endef

define Package/rjserver/description
An fake ruijie server
endef

define Package/rjserver/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/rjserver $(1)/usr/sbin/
	chmod 755 $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,rjserver))
