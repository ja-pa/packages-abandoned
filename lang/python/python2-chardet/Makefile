#
# Copyright (C) 2007-2017 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python2-chardet
PKG_VERSION:=3.0.4
PKG_RELEASE:=2
PKG_LICENSE:=LGPL-2.1

PYPI_NAME:=chardet
PKG_HASH:=84ab92ed1c4d4f16916e05906b6b75a6c0fb5db821cc65e70cbd64a3e2a5eaae

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python2-package.mk

define Package/python-chardet/Default
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  MAINTAINER:=Alexandru Ardelean <ardeleanalex@gmail.com>
  URL:=https://github.com/chardet/chardet
endef

define Package/python2-chardet
$(call Package/python-chardet/Default)
  TITLE:=Universal encoding detector for Python 2
  DEPENDS:=+PACKAGE_python2-chardet:python2
  VARIANT:=python2
endef

define Package/python2-chardet/description
  Universal encoding detector for Python 2 and 3
endef

define Py3Package/python2-chardet/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(PKG_INSTALL_DIR)/usr/bin/* $(1)/usr/bin/
	for bin in $(1)/usr/bin/*; do \
		mv $$$$bin $$$${bin}2 ; \
	done
endef

$(eval $(call Py2Package,python2-chardet))
$(eval $(call BuildPackage,python2-chardet))
$(eval $(call BuildPackage,python2-chardet-src))
