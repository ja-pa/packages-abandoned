#
# Copyright (C) 2007-2017 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python2-urllib3
PKG_VERSION:=1.25.7
PKG_RELEASE:=1

PKG_MAINTAINER:=Josef Schlehofer <pepe.schlehofer@gmail.com>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.txt
PKG_CPE_ID:=cpe:/a:urllib3_project:urllib3

PYPI_NAME:=urllib3
PKG_HASH:=f3c5fd51747d450d4dcf6f923c81f78f811aab8205fda64b0aba34a4e48b0745

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python2-package.mk

define Package/python-urllib3/Default
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Sanity-friendly HTTP client
  URL:=https://urllib3.readthedocs.io/
endef

define Package/python2-urllib3
$(call Package/python-urllib3/Default)
  DEPENDS:=+PACKAGE_python2-urllib3:python2
  VARIANT:=python2
endef

define Package/python2-urllib3/description
  HTTP library with thread-safe connection pooling, file post, and more.
endef

$(eval $(call Py2Package,python2-urllib3))
$(eval $(call BuildPackage,python2-urllib3))
$(eval $(call BuildPackage,python2-urllib3-src))
