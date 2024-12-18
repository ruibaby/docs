---
title: 插件
description: 插件管理相关功能说明
---

插件是用于扩展 Halo 功能的软件包。插件独立于 Halo 核心应用，可以单独安装、升级、卸载。

本文档仅对插件的基本管理功能进行说明，关于插件的详细使用说明请参考对应插件的文档。

:::info
目前有两个官方渠道可以获取插件：

- 应用市场：[https://www.halo.run/store/apps](https://www.halo.run/store/apps)
- Awesome Halo：[https://github.com/halo-sigs/awesome-halo](https://github.com/halo-sigs/awesome-halo)

:::

## 安装插件

进入插件管理页面，点击右上角的 `安装` 按钮即可打开插件安装的对话框。

### 从内置应用市场安装（推荐）

从 Halo 2.10 开始，内置了应用市场插件，可以更加方便在 Console 直接安装应用市场的插件。

![安装插件](/img/user-guide/app-store/app-store-plugins.png)

:::info
更多关于内置应用市场的使用说明可查阅：[应用市场](./app-store.md)
:::

### 本地上传安装

![安装插件](/img/user-guide/plugins/plugin-install.png)

插件安装成功后，便会出现在插件管理的列表中。

:::info 注意
从非 Halo 官网应用市场安装插件时，请务必注意其安全性。
:::

### 远程下载安装

同样，在安装插件的对话框中，切换到远程下载选项卡，输入插件的下载地址，点击 `下载` 按钮即可开始下载插件。

:::info 注意
从非 Halo 官网应用市场安装插件时，请务必注意其安全性。
:::

## 插件设置

点击插件列表中的某个插件进入插件详情页面。与主题设置类似，插件详情页面默认显示出了当前插件的详细信息，在详细信息标签页后方的标签页，即为插件提供的相关设置。不同的插件提供的设置项各不相同，设置项的详细说明请参考对应插件的文档。

![插件设置](/img/user-guide/plugins/plugin-setting.png)

此处以 `Umami` 插件为例。

:::info
你可以点击插件列表指定插件所在行后方的 `···` 更多操作按钮，选择其中的 `重置` 选项将插件提供的设置项恢复为默认值。
:::

## 启用/禁用插件

点击插件列表或插件详情页中的启用/禁用开关，即可切换插件的启用禁用状态。

![插件启用/禁用](/img/user-guide/plugins/plugin-switch.png)

## 升级插件

如果当前使用了内置的应用市场插件，在插件更新后会在插件列表中显示更新提示，点击 **立即更新** 按钮即可。

手动升级可以点击具体插件的 `···` 更多操作按钮，选择其中的 `升级` 选项即可打开升级插件的对话框。

## 重置

如果你需要清空所有插件配置并重新配置插件，你可以通过 `···` 更多操作中的 `重置` 选项将主题提供的设置项恢复为默认值。

## 卸载插件

点击插件列表指定插件所在行后方的 `···` 更多操作按钮，选择其中的 `卸载` 选项即可对当前插件进行卸载。

![卸载插件](/img/user-guide/plugins/plugin-uninstall.png)

:::info
目前提供了 `卸载` 及 `卸载并删除配置` 两种卸载方式。
仅卸载插件时插件的配置信息会进行保留，当重新安装插件后还可以使用之前已保存的配置。
:::

## 扩展配置

在 Halo 的插件机制中，我们使用扩展点来实现插件与 Halo 核心应用的交互，插件可以通过扩展点来扩展 Halo 的功能。这就意味着插件可能会实现和 Halo 或者其他插件相同的扩展点，这时候就需要对扩展点进行管理。

以搜索引擎为例，Halo 默认提供了 `Lucence` 搜索引擎和对应的扩展点，那么用户在安装了其他搜索引擎插件之后就需要在这里进行选择，否则 Halo 无法确定使用哪个搜索引擎。

![Extension point settings entry](/img/user-guide/plugins/extension-point-settings-entry.png)

进入插件管理，点击右上角的 `扩展配置` 按钮即可进入扩展配置页面。

![Extension point settings](/img/user-guide/plugins/extension-point-settings.png)

这里以搜索引擎为例，安装了 `Meilisearch` 插件之后就可以在这里选择启用这个插件的搜索引擎。

更多关于扩展点的说明可以查阅：[插件开发 / 扩展点和定制化 / 扩展点](../developer-guide/plugin/extension-points/server/index.md)
