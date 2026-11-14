# android_device_xiaomi_xun-kernel

Prebuilt kernel set for the Xiaomi Redmi Pad SE (`xun`), maintained for the
personal LineageOS 22.2 port at <https://github.com/robsonsilv4/lineageos-xun>.

The repository is standalone. It started as a fork of
[Xiaomi-Redmi-Pad-SE-Resources/android_device_xiaomi_xun-kernel](https://github.com/Xiaomi-Redmi-Pad-SE-Resources/android_device_xiaomi_xun-kernel),
which is archived, and `lineage-22.2` continues from that tree at
`8f9e2bca3107337a822599daf4394c8719adb3cb`.

The branch carries the kernel set from OS2.0.209.0.VMUMIXM: the kernel image,
the six device trees, `dtbo.img` and the 469 modules. They ship together
because a module only loads against the kernel build that produced it; the
package is the unit, not the `vermagic` string. The set replaces the 204
prebuilts the device tree was written against.

The manifest pins the build commit, the parent of the commit that added this
README. Do not force-push `lineage-22.2`. The kernel choice and its limits are
in `docs/decisions/0001-blob-rebase-209.md` in the port repository.
