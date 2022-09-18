<p align="center">
 <img width="150px" src="assets/devbook.svg" align="center" alt="Devbook" />
 <h2 align="center">开发手册</h2>
 <p align="center">开发前需要阅读和知晓的一些内容</p>
</p>
<p align="center">
  <a href="http://buildingdata.xauat.edu.cn/">
  	<img alt="http://buildingdata.xauat.edu.cn/" src="https://img.shields.io/badge/数据平台-063c7c?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAUCAYAAACNiR0NAAAACXBIWXMAAAsTAAALEwEAmpwYAAABQ0lEQVQ4jZ3UPU8UURjF8d8ubwmhopGAQKSDymhjQWm30hEbwkthgV9AQkUJFq5+AyVsIYXfwspADRWSYAMfgIIQH4qdjZv1zp1lT3Izd86c88/cZJ6pRYQ+9BY1HFcmI6JqvYl/WqnKV8Ga8b+agwCfRcRpAtbRaUQs9AvcyIB6tVkF/PYIWEeHKeCLiLgYANbR74JBRGxXhP9ExExEzEbEVUX2fR0rma/qEk/xCg3M4jyTbwzjOhNYwBpaxf0cFlE2DTf1DOxzUWx1ebuYLq4p1XLAA6wm/H18Len8zQFv8DrhL2u/+X3i2V0OCGMJ7x4j2j+LXmWPPIFfCf8E4xhKlXLALRwm/D08LyvlgJ9wi6Mev4GdQYCj+IgNnHX5X/CyrFPHkwz0A9axhO+ZXEdTw/ihfFrGMVns32mP3XwG+PMBYdAQPwkBdngAAAAASUVORK5CYII=&logoColor=white" />
  </a>
  <a href="https://github.com/buildingdata">
  	<img alt="Github" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <img alt="icon" src="https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fbuildingdata&label=View&labelColor=%23222222&countColor=%2337d67a" />
</p>


### 📐 开发规则

#### 1.仓库的权限和配额

##### 1.1 仓库的权限

- **开源：** 一般的普通代码
- **私库：** 核心代码、专利软件等

##### 1.2 组织的配额

目前配额如下，后续会考虑进行升级：

- 无限数量的 public/private repos
- 无限数量的合作者
- 每月 2000 分钟的 Github Actions 运行时间
- 500MB 包存储空间
- 社区支持

#### 2.仓库的主分支

由于众所周知的原因，Github 在 2020 年 10 年 1 日宣布，所有的新 repo 主分支更改为 `main` 取代原来的 `master` 名称，所以小伙伴们注意检查下自己客户端的 **default branch name** 是否是 `main` 名称。

#### 3.代码提交

代码提交前一定要对代码进行审查，避免冲突过多。提交的 commit 信息，使用简短的中文说明即可。

🔍 详情可参考 Github 文档：

- [审查拉取请求中的建议更改](https://docs.github.com/cn/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/reviewing-proposed-changes-in-a-pull-request)
- [管理团队的代码审查设置](https://docs.github.com/cn/organizations/organizing-members-into-teams/managing-code-review-settings-for-your-team#about-code-review-settings)

#### 4.仓库的命名

仓库的名称命名我们采用了 **“小写字母加短横线”** 和 **“大驼峰”** 的命名规则，细则如下：

```
# 小写字母加短横线，这种方式一般适用于较小的项目代码和脚本
# 例如：
- python-netcdf4
- python-xarray

# 大驼峰命名，这种方式一般适用单个单词、软件和工具开发
# 例如：
- Welcome
- Logo
- EnergyCalculating
- PowerToys
```

#### 5.忽略文件规则

为了减少一些无关文件的推送，建议使用如下的 `.gitignore` 配置文件规则：

```gitignore
# Windows image file caches
Thumbs.db
ehthumbs.db

# Folder config file
Desktop.ini

# Recycle Bin used on file shares
$RECYCLE.BIN/

# Windows Installer files
*.cab
*.msi
*.msm
*.msp

# Windows shortcuts
*.lnk

# =========================
# Operating System Files
# =========================

# OSX
# =========================

*/.DS_Store
.DS_Store
.LSOverride
.AppleDouble

# Thumbnails
._*

# Files that might appear in the root of a volume
.DocumentRevisions-V100
.fseventsd
.Spotlight-V100
.TemporaryItems
.Trashes
.VolumeIcon.icns

# Directories potentially created on remote AFP share
.AppleDB
.AppleDesktop
Network Trash Folder
Temporary Items
.apdisk
```

### 6.README 自述文件

#### 6.1 README 拟写规则

建议每个 repo 都要写一份 README 自述文件，可以帮助其余同学理解和使用，避免踩坑和节省时间。

README 自述文件格式就按照论文序号格式按序标注即可（一级标题带 `.`，二三级标题使用一个空格）。由于 Github 对 Markdown 的 `h1` 和 `h2` 标签样式会添加一个分割线，故除了大标题外，建议使用  `h3` ，`h4` 和 `h5` 三个标签，示例如下：

```markdown
## 大标题

### 1.一级标题
#### 1.1 二级标题
##### 1.1.1 三级标题
#### 1.2 二级标题

### 2.一级标题
```

#### 6.2 README 资产归类

我们在拟写 README 自述文件的时候，常常会需要图片的引用，有时候引用的图片会比较多，请在此代码仓库的根目录下新建 `assets` 文件夹用于存放图片和其他。例示目录层级如下：

```
├── assets/
    ├── logo.svg          // 例示 Logo 文件
    ├── banner.png        // 例示图片文件
    ├── img/              // 你还可以细化分类目录
└── README.md
```

#### 6.3 README 深色模式（可选）

Github 已经支持深色模式，很多小伙伴们也都很喜欢设置为深色主题。如果你想让自己的 README 好看些，可以准备浅色和深色两套素材，然后使用 Github 提供的标签 `#gh-light-mode-only` 和 `#gh-dark-mode-only`，来根据你的当前主题进行素材的切换。例子如下：

```markdown
![Light](assets/light.png#gh-light-mode-only)
![Dark](assets/dark.png#gh-dark-mode-only)
```

#### 6.4 README Issue 模板（可选）

Github 支持自定义 Issue 模板，如果你需要的话，可以自行设定。几个 [Issue 模板](https://github.com/buildingdata/Welcome/issues)在此仓库的 `.github/ISSUE_TEMPLATE` 下，需要的可自取。

### 🔍 遇到问题

- 可以查看团队的 Wiki
- 可以到团队讨论发起问题
- 遇到 bug 或问题可以到相应的 repo 提交 Issue
