#
# Copyright (C) 2007-2017 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python2-django-restframework39
PKG_VERSION:=3.9.4
PKG_RELEASE:=1

PYPI_NAME:=djangorestframework
PKG_HASH:=c12869cfd83c33d579b17b3cb28a2ae7322a53c3ce85580c2a2ebe4e3f56c4fb

PKG_MAINTAINER:=Alexandru Ardelean <ardeleanalex@gmail.com>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE.md

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python2-package.mk

define Package/django-restframework39/Default
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Web APIs for Django, made easy.
  URL:=https://www.django-rest-framework.org
endef

define Package/python2-django-restframework39
$(call Package/django-restframework39/Default)
  DEPENDS:= \
	+PACKAGE_python2-django-restframework39:python2 \
	python2-django1
  VARIANT:=python2
  MDEPENDS:=python2-django1
endef

define Package/python2-django-restframework39/description
  Web APIs for Django, made easy. (3.9 series)
endef

$(eval $(call Py2Package,python2-django-restframework39))
$(eval $(call BuildPackage,python2-django-restframework39))
$(eval $(call BuildPackage,python2-django-restframework39-src))
