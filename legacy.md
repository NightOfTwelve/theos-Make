
导入 FRAMEWORK 变量定义，用户工程是作为FrameWork编译安装;
legacy.mk中的变量定义多为递归展开式变量赋值；
从theos系列变量中导入多数变量为Framework系列；

```make
FRAMEWORKDIR = $(THEOS)
FW_BINDIR = $(THEOS_BIN_PATH)
FW_MAKEDIR = $(THEOS_MAKE_PATH)
FW_INCDIR = $(THEOS_INCLUDE_PATH)
FW_LIBDIR = $(THEOS_LIBRARY_PATH)
FW_MODDIR = $(THEOS_MODULE_PATH)

FW_PROJECT_DIR = $(THEOS_PROJECT_DIR)
```

以下多数变量在legacy.mk被首次引入时，尚未定义
略去部分条件判断逻辑：
```make
FW_STAGING_DIR = $(THEOS_STAGING_DIR)
FW_BUILD_DIR = $(THEOS_BUILD_DIR)
FW_OBJ_DIR = $(THEOS_OBJ_DIR)
FW_SUBPROJECT_PRODUCT = $(THEOS_SUBPROJECT_PRODUCT)

FW_INSTANCE = $(THEOS_CURRENT_INSTANCE)

FW_SHARED_BUNDLE_RESOURCE_PATH = $(THEOS_SHARED_BUNDLE_RESOURCE_PATH)
FW_PACKAGE_NAME = $(THEOS_PACKAGE_NAME)
FW_PACKAGE_ARCH = $(THEOS_PACKAGE_ARCH)
FW_PACKAGE_VERSION = $(THEOS_PACKAGE_BASE_VERSION)
FW_PACKAGE_DEBVERSION = $(THEOS_PACKAGE_VERSION)
FW_PACKAGE_FILENAME = $(THEOS_PACKAGE_FILENAME)

```
