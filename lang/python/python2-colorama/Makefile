include $(TOPDIR)/rules.mk

PKG_NAME:=python2-colorama
PKG_VERSION:=0.4.1
PKG_RELEASE:=1

PYPI_NAME:=colorama
PKG_HASH:=05eed71e2e327246ad6b38c540c4a3117230b19679b875190486ddd2d721422d

PKG_MAINTAINER:=Daniel Danzberger <daniel@dd-wrt.com>
PKG_LICENSE:=MIT

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python2-package.mk

define Package/python-colorama/Default
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=colorama
  URL:=https://github.com/tartley/colorama
endef

define Package/python2-colorama
$(call Package/python-colorama/Default)
  DEPENDS:=+PACKAGE_python2-colorama:python2
  VARIANT:=python2
endef

define Package/python2-colorama/description
Makes ANSI escape character sequences
(for producing colored terminal text and cursor positioning) work under MS Windows.
endef

$(eval $(call Py2Package,python2-colorama))
$(eval $(call BuildPackage,python2-colorama))
$(eval $(call BuildPackage,python2-colorama-src))
