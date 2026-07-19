KBUILD_OPTIONS += CONFIG_TOUCHSCREEN_FTS=m
KBUILD_OPTIONS += KBUILD_EXTRA_SYMBOLS=$(abspath $(OUT_DIR))/../sm7435-modules/fcnt/huaqinhardware_info/Module.symvers

all: modules

modules_install:
	$(MAKE) INSTALL_MOD_STRIP=1 -C $(KERNEL_SRC) M=$(M) modules_install

%:
	$(MAKE) -C $(KERNEL_SRC) M=$(M) $@ $(KBUILD_OPTIONS)
