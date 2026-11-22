# apm-local-wallpaper-skin

电梓播放器（APM / Azusa Player Mobile）自定义皮肤：**外观与官方内置主题「电闹播放器」完全一致**，只把主播放页壁纸换成你自己的手机本地图片。

## 用法

1. 复制 raw 链接：
   `https://raw.githubusercontent.com/wasatio/apm-local-wallpaper-skin/main/apm-local-wallpaper-skin.json`
2. APM → 设置 → 外观 → 顶部输入框粘贴该链接 → 回车
3. 在皮肤列表里点一下「本地壁纸·电闹」应用
4. 仍停留在「外观」页 → 点 **选择照片** → 从相册选一张图，即成为壁纸

## 注意

- 皮肤 JSON 无法直接引用本地图片：iOS 的 `ph://`、Android 的 `content://` 都无法跨设备，所以壁纸必须由 App 内的「选择照片」设置，它会把图片 URI 写进当前皮肤。
- **切换皮肤会重置本地壁纸**，切换之后需要重新选一次照片。
- `backgroundImages` 保持空数组，避免任何网络图盖掉本地壁纸；横屏会自动复用同一张图。
- 配色、表情条、播放键样式均取自官方内置主题，未作改动。

## 版权与许可

- 本仓库的皮肤配置（`colors`、`customColors`、`gifs` 等）取自
  [lovegaoshi/azusa-player-mobile](https://github.com/lovegaoshi/azusa-player-mobile) 的
  `src/components/styles/NoxTheme.ts`。该项目以 **AGPL-3.0** 许可发布，故本仓库同样以
  AGPL-3.0 发布，许可证全文见 [LICENSE](LICENSE)。
- `gifs` 以及 `metaData.themeIcon` 指向的图片，版权归 **哔哩哔哩（bilibili）** 及相应主播 /
  UP 主所有。本仓库**仅以 URL 引用，未复制、未再分发任何图片本体**。
- 本皮肤仅供**个人非商业使用**。请勿用于收费、打包发行，或任何暗示官方授权 / 官方出品的用途；
  涉及主播形象的二次创作请遵守该主播的规约。
- 「电梓播放器 / APM」名称与标识归其作者所有，本仓库与其无隶属关系，亦未获其背书。

皮肤 JSON 的完整字段定义见上游仓库 `src/types/style.d.ts`。
