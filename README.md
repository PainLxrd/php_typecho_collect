# Typecho主题合集26套_免费下载

![主题数量](https://img.shields.io/badge/主题-26套-blue)
![费用](https://img.shields.io/badge/费用-免费分享-brightgreen)
![更新](https://img.shields.io/badge/状态-持续更新-orange)

个人建站第一步是选主题：博客、视频站、导航站、壁纸站，不同玩法对应不同主题。本仓库共整理 **26套Typecho主题/源码**，博客自媒体、视频站、导航站、壁纸站、社交圈子、APP源码全覆盖，下载后先看各包根目录 `README.md`，按步骤安装。

> 完整图文版（含重点主题详解、伪静态配置、问题对照表）：[网盘资源社_Typecho主题合集26套](https://www.wpzys.cn/a/27)

## 📦 完整清单（点击展开）

<details>
<summary>26套主题一句话介绍</summary>


| 主题                    | 类型       | 一句话介绍                          |
| ----------------------- | ---------- | ----------------------------------- |
| Spimes X7.0             | 自媒体博客 | 小灯泡自媒体博客主题，需配Deng插件  |
| Spimes X5.0             | 自媒体博客 | X5.0主题+Typecho程序+Deng插件合集包 |
| Spimes X4.6             | 自媒体博客 | 无加密无授权版，需配Deng插件        |
| Joe                     | 博客       | Typecho热门博客主题，功能全面       |
| Joe二次开发美化版 V1.30 | 博客       | Joe主题美化二开版，开箱即用         |
| Handsome 6.0            | 博客       | 友人C经典主题，建站热门选择         |
| Ginto                   | 门户博客   | 响应式门户，自带海报生成与弹幕组件  |
| DUX                     | 博客资讯   | 仿大前端DUX风格，适合资讯站         |
| Aria                    | 博客       | 简洁书写风，支持Pjax与MathJax       |
| BestGirl                | 博客       | 秀气女性向主题，带音乐播放器        |
| Brave                   | 情侣博客   | 情侣恋爱记录站整站包                |
| DearLicy                | 博客       | 小清新风格博客主题                  |
| Freewind                | 博客       | 自由之风主题，仅建议学习研究        |
| Single                  | 博客       | 清新博客主题，带夜间模式            |
| Bubble                  | 博客       | 清新响应式网站主题                  |
| StarrySky               | 博客       | 星空风格博客主题（两版任选）        |
| wenso                   | 博客       | 纯文字极简主题，轻量快速            |
| VOID                    | 博客       | V3.5.1简约博客主题                  |
| Kratos                  | 博客       | 由WordPress移植而来的简洁主题       |
| ZeVideo                 | 视频站     | 视频主题整站包，自带CatClaw采集插件 |
| WebStack                | 导航站     | 设计导航主题，支持自定义排序        |
| Wallpaper               | 壁纸站     | 壁纸头像站手机版主题                |
| Fresh                   | 后台主题   | 扁平化自适应Typecho后台主题         |
| RuleApp                 | APP源码    | 博客社区资讯APP，Typecho做后端      |
| OneClrle                | 社交圈子   | 社交圈子主题，另附三款配套插件      |

</details>

## ⭐ 重点推荐

- **Spimes X7.0**：自媒体首选，文章聚合+投稿+弹幕播放器，强依赖Deng插件（包内自带），弹幕需单独建库。
- **Joe / 二开版**：装机量最大的Typecho主题之一，新手先用原版跑通，再换二开版。
- **Handsome 6.0**：时光机、书单、电影单全了，适合长期经营个人品牌。
- **ZeVideo**：视频站一条龙（程序+主题+采集插件），整站上传后走 `/install.php` 全新安装。
- **WebStack**：网址导航布局，后台自定义排序，配个短域名效果最好。
- **Wallpaper**：手机壁纸站，长按保存是核心玩法，吃移动端流量。

## 🛠️ 安装步骤

1. 上传主题目录到网站的 `usr/themes/` 文件夹；
2. 登录后台，在“更换外观”里启用主题；
3. 主题若提示缺插件（如Spimes要Deng），到“插件管理”启用包内自带插件；
4. 按各包根目录 `README.md` 的说明，新建导航、留言板等独立页面并填缩略名；
5. 前台刷新看效果，再进主题设置逐项填写站点信息。

整站包（Brave、ZeVideo）不走上面流程：整站上传后直接访问 `/install.php` 按向导安装。

运行环境一般为 PHP5.6+ / MySQL5.6+，版本说明可对照 [Typecho官网](https://typecho.org)。

## 🔧 伪静态配置（必做，否则分类页404）

Apache（.htaccess）：

```apache
RewriteEngine On
RewriteBase /
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ /index.php/$1 [L]
```

Nginx：

```nginx
location / {
    index index.php index.html;
    if (!-e $request_filename) {
        rewrite ^(.*)$ /index.php$1 last;
    }
}
```

## ❓ 常见问题

- **26套都要装吗？** 不用，一次只启用一套，先缩小到两三套试一遍再定，换主题不丢文章和数据。
- **主题和插件版本对不上？** 以各包内自带的组合为准，不要跨包混用不同版本的Deng。
- **分类/文章页404？** 没配伪静态，按上一节配对应环境的规则。
- **Spimes提示缺插件/弹幕发不出去？** 启用包内Deng插件，弹幕库按包内README建库并改默认密码。
- **手机端效果差？** 优先选响应式：Ginto、Wallpaper、Single、Bubble。

## 🔗 更多免费资源

- 图文详解版：[网盘资源社_Typecho主题合集26套](https://www.wpzys.cn/a/27)
- 毕业设计建站：[Java毕设源码大全](https://www.wpzys.cn/a/5)（1400+套SpringBoot毕设源码免费分享）

## ⚠️ 声明

本仓库内容仅供学习交流，请勿用于商业用途；采集类功能请只用在正规内容上；Freewind包后台设置文件有缺损，仅适合学习研究。
