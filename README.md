# Night Lights 网易基岩版移植资源包

Pixovate 把 Night Lights 模组移植到网易我的世界基岩版时用的资源包（移植工程里的 `res/`）。原模组以 LGPLv3 发布，资源包里的模型、贴图和方块名称都由原模组的资源转换而来，按同一许可证单独公开。

贴图在子模块 `textures/nightlights/` 里（单独的仓库 <https://github.com/Pixovate/night-lights-netease-textures>），克隆时带上子模块：

```
git clone --recursive https://github.com/Pixovate/night-lights-netease-resource-pack.git
```

## 来源

- 原模组：Night Lights，作者 Joosh、samgj15，<https://github.com/bonsaistudi0s/night-lights>
- 移植时对照的源码：<https://github.com/Pixovate/night-lights>，提交 `6357c2b09e0c9f6937d0313142f731a1f17462a5`
- 许可证：原模组 `META-INF/mods.toml` 声明 `LGPLv3`

## 内容与改动

| 路径 | 说明 |
| --- | --- |
| `models/blocks/nightlights/*.geo.json` | 原模组 `assets/nightlights/models/block/` 的方块模型换算成基岩版几何体（坐标、旋转和 UV 换算，完全相同的模型合用一份）。`night_light_frog`、`night_light_octopus` 换算后又手工调整过（Pixovate，2026-10-09） |
| `textures/nightlights/` | 贴图子模块：原模组 82 张方块贴图原样复制，另加创造物品栏分页图标，说明见子模块里的 README.md |
| `textures/terrain_texture.json`、`blocks.json` | 贴图索引和方块声音，按原模组的方块列表生成 |
| `texts/en_US.lang` | 方块名称取自原模组 `lang/en_us.json`，另加创造物品栏分页和分组名 |
| `texts/zh_CN.lang` | 中文名称是移植时新翻译的（原模组没有中文） |
| `manifest.json` | 网易资源包清单，移植时新写的 |

## 许可证

本仓库以 GNU 宽通用公共许可证第 3 版（LGPLv3）授权，见 [COPYING.LESSER](COPYING.LESSER)；它是在 GNU 通用公共许可证第 3 版之上附加的条款，见 [COPYING](COPYING)。

---

# Night Lights resource pack for the NetEase Bedrock port

The resource pack used by Pixovate's port of the Night Lights mod to the NetEase edition of Minecraft Bedrock (`res/` in the port). The original mod is released under the LGPLv3; the models, textures and block names here are converted from its assets, so this pack is published separately under the same license.

Textures live in the submodule `textures/nightlights/` (separate repository <https://github.com/Pixovate/night-lights-netease-textures>); clone with `--recursive`.

- Original mod: Night Lights by Joosh and samgj15, <https://github.com/bonsaistudi0s/night-lights>
- Source used for the port: <https://github.com/Pixovate/night-lights> at commit `6357c2b09e0c9f6937d0313142f731a1f17462a5`
- License declared in the original `META-INF/mods.toml`: `LGPLv3`

Changes: `models/blocks/nightlights/*.geo.json` are the original block models from `assets/nightlights/models/block/` converted to Bedrock geometry (coordinates, rotations and UVs converted; identical models share one file); `night_light_frog` and `night_light_octopus` were adjusted by hand afterwards (Pixovate, 2026-10-09). `textures/terrain_texture.json` and `blocks.json` are generated from the original block list. `texts/en_US.lang` takes the block names from the original `lang/en_us.json` and adds creative tab and group names; `texts/zh_CN.lang` is a new Chinese translation. `manifest.json` is new.

Licensed under the GNU Lesser General Public License v3.0 ([COPYING.LESSER](COPYING.LESSER)), which supplements the GNU General Public License v3.0 ([COPYING](COPYING)).
