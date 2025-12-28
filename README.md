# caddy-naive-build

本仓库使用 GitHub Action 云编译适用于 aarch64 架构，带有 [Forward proxy](https://github.com/klzgrad/forwardproxy) 插件的 Caddy 二进制文件。可用作 NaïveProxy 服务端。

您可以从 [Release](https://github.com/zwzheng45/caddy-naive-build/releases) 中获取最新编译的二进制文件。

> [!NOTE]
>
> 经过测试，编译出的文件可以在`aarch64_cortex-a53`架构，运行 OpenWrt 的路由器上正常工作，理论上能兼容大多 aarch64 架构的设备。

您也可以 fork 本仓库，修改 [build-caddy-naive-openwrt-arm64.yml](.github/workflows/build-caddy-naive-openwrt-arm64.yml) 中的目标平台，并自行进行编译。

