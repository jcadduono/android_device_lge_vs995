## TWRP device tree for LG V20 (Verizon Wireless VS995)

Add to `.repo/local_manifests/vs995.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/lge/vs995" name="android_device_lge_vs995" remote="TeamWin" revision="android-6.0" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_vs995-eng
make -j5 recoveryimage
```

Kernel sources are available at: https://github.com/jcadduono/android_kernel_lge_msm8996/tree/twrp-7.0

