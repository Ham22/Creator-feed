include $(TOPDIR)/rules.mk

PKG_NAME:=python3-letmecreate
PKG_VERSION:=1.2.1

PKG_SOURCE_VERSION:=v$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/francois-berder/PyLetMeCreate.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)

PKG_LICENSE_FILE:=LICENSE
PKG_LICENSE:=BSD-3-Clause
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_INSTALL:=1
PKG_BUILD_DEPENDS:=python3

include $(INCLUDE_DIR)/package.mk

define Package/python3-letmecreate
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=PyLetMeCreate
  URL:=https://github.com/francois-berder/PyLetMeCreate
  DEPENDS:= +python3-light +letmecreate
endef

define Package/python3-letmecreate/description
	Python binding of LetMeCreate library.
endef

define Build/Compile
endef

define Build/Install
endef

define Package/python3-letmecreate/install
	$(INSTALL_DIR) $(1)/usr/bin/pyletmecreate_examples/
	$(CP) $(PKG_BUILD_DIR)/examples/*.py $(1)/usr/bin/pyletmecreate_examples/

	$(INSTALL_DIR) $(1)/usr/lib/python3.5/site-packages/
	$(CP) $(PKG_BUILD_DIR)/letmecreate $(1)/usr/lib/python3.5/site-packages/
endef

$(eval $(call BuildPackage,python3-letmecreate))

