# Build N60 Pro 512M

这个仓库用于通过 GitHub Actions 云编译磊科 `Netcore N60 Pro` 硬改 `512MB SPI-NAND` 的 OpenWrt 主线 `v25.12.1` 固件。

实现方式：

- 源码使用官方 `openwrt/openwrt` 的 `v25.12.1`
- 在官方已支持的 `Netcore N60 Pro` 基础上补一个 `512ROM` 机型变体
- `512M` 变体思路参考了 `moshanghuakai01/netcore-n60-pro` 仓库中基于 `dailook` 源码的做法，但补丁已经按 OpenWrt 主线 `filogic` 目录结构重写

工作流触发方式：

- 推送到 `main` 或 `master`
- 在 Actions 页面手动运行 `build-openwrt-25.12.1-n60-pro-512rom`

编译产物会以 GitHub Actions Artifact 形式上传。
