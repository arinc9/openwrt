#
# Copyright (C) 2020-2021 Ycarus (Yannick Chabanois) <ycarus@zugaina.org>
# Copyright (C) Arınç ÜNAL <arinc.unal@arinc9.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ell
PKG_VERSION:=0.66
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cdn.kernel.org/pub/linux/libs/ell
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_HASH:=7a78b757080ed6518c1c4fa26ad6a7a3d6e4e385386a20b6fb52379e7d1ffa36

PKG_LICENSE:=GPL-2.0
PKG_LICENSE_FILES:=GPL

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/libell
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=Embedded Linux library
  URL:=https://git.kernel.org/pub/scm/libs/ell/ell.git
endef

define Package/libell/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libell*.so* $(1)/usr/lib
endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)
	$(CP) $(PKG_INSTALL_DIR)/* $(1)/
endef

$(eval $(call BuildPackage,libell))
