# caddy-naive-build

本仓库使用 GitHub Action 云编译适用于 aarch64 架构，带有 [Forward proxy](https://github.com/klzgrad/forwardproxy) 插件的 Caddy 二进制文件。可用作 NaïveProxy 服务端。

您可以从 [Release](https://github.com/zwzheng45/caddy-naive-build/releases) 中获取最新编译的二进制文件。

> [!NOTE]
>
> 经过测试，编译出的文件可以在`aarch64_cortex-a53`架构，运行 OpenWrt 的路由器上正常工作，理论上能兼容大多 aarch64 架构的设备。

Release 中提供两个版本的 Caddy，使用了不同的 Forward proxy 插件编译：

1. `naive`版本使用 [klzgrad/forwardproxy](https://github.com/klzgrad/forwardproxy)，这是 NaïveProxy 官方维护的插件。
2. `udpintcp`版本使用 [aUsernameWoW/forwardproxy](https://github.com/aUsernameWoW/forwardproxy/tree/udpintcp)，相较于官方插件额外支持了 sing-box 的 [UDP over TCP v1/v2](https://sing-box.sagernet.org/zh/configuration/shared/udp-over-tcp/)。

有关 NaïveProxy 中 UDP over TCP 的更多信息，请移步[这个 issue](https://github.com/klzgrad/naiveproxy/issues/617)。

您也可以 fork 本仓库，使用或修改 [build-caddy-naive-openwrt-arm64.yml](.github/workflows/build-caddy-naive-openwrt-arm64.yml) 并自行进行编译。

