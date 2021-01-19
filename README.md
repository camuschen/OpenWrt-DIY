[![如页面部分图片无法显示，请直接点这里到末尾看修复教程](https://visitor-badge.glitch.me/badge?page_id=OpenWrt-DIY-visitor-badge)](#解决-github-网页上图片显示失败的问题) [![](https://img.shields.io/github/stars/IvanSolis1989/OpenWrt-DIY?color=FFFFFF)](https://github.com/IvanSolis1989/OpenWrt-DIY/stargazers) [![](https://img.shields.io/github/forks/IvanSolis1989/OpenWrt-DIY?color=FFFFFF)](https://github.com/IvanSolis1989/OpenWrt-DIY/network/members) [![](https://img.shields.io/github/release-date/IvanSolis1989/OpenWrt-DIY?color=FFFFFF&label=%E6%9B%B4%E6%96%B0%E6%97%A5%E6%9C%9F)](https://github.com/IvanSolis1989/OpenWrt-DIY/actions) [![](https://img.shields.io/badge/QQ群-点击加入-FFFFFF.svg)](https://jq.qq.com/?_wv=1027&k=9Sh2iNhT)
<a href="#readme">
    <img src="https://img.vim-cn.com/48/6e4b91fdeefa201f93befdf858a13eefeaff5c.jpg" alt="图裂了😂" title="OpenWrt-DIY" align="right" height="180" />
</a>

[OpenWrt DIY — 多设备固件云编译](https://jq.qq.com/?_wv=1027&k=9Sh2iNhT)
======================

[![](https://img.shields.io/badge/-目录:-696969.svg)](#readme) [![](https://img.shields.io/badge/-基本介绍-F5F5F5.svg)](#基本介绍-) [![](https://img.shields.io/badge/-近期更新-F5F5F5.svg)](#近期更新-) [![](https://img.shields.io/badge/-注意事项-F5F5F5.svg)](#注意事项-) [![](https://img.shields.io/badge/-OpenWrt小贴士-F5F5F5.svg)](#openwrt-小贴士-) [![](https://img.shields.io/badge/-赞助本项目-F5F5F5.svg)](#赞助支持本项目-) [![](https://img.shields.io/badge/-鸣谢-F5F5F5.svg)](#鸣谢-)

请 **认真阅读完毕** 本页面，本页面包含如何提升固件下载体验的内容。

如果您未阅读完本页面，可能会遇到 **固件下载问题** ，若遇到问题，请 **返回此页面，认真完整阅读一遍** ~

<p align="center"><img src="https://img.shields.io/badge/-支持设备、编译状态及固件下载-FFFFFF.svg" height="35" alt="图裂了😂"/></p>

**点击下表中 [![](https://img.shields.io/badge/设备-passing-32CD32.svg)](https://github.com/IvanSolis1989/OpenWrt-DIY/actions) 即可跳转到该设备固件下载页面** 

|    序号   |     设备平台     |   编译状态及下载链接 |   插件配置   | 备注说明   |
| :-----------------: | :-------------: |:-----------------: | :-----------------: |  :-----------------: | 
| 1 |   [![](https://img.shields.io/badge/OpenWrt-x86_64_(64位)-FFFFFF.svg)](https://github.com/camuschen/OpenWrt-DIY/actions?query=workflow%3A%22Build+X86%2864bit%29+OpenWrt%22)    | [![](https://github.com/camuschen/OpenWrt-DIY/workflows/Build%20X86(64bit)%20OpenWrt/badge.svg)](https://github.com/camuschen/OpenWrt-DIY/actions?query=workflow%3A%22Build+X86%2864bit%29+OpenWrt%22) |[![](https://img.shields.io/badge/编译-配置-orange.svg)](https://github.com/camuschen/OpenWrt-DIY/blob/main/config/x86_64.config) |  |  
| 2 |      [![](https://img.shields.io/badge/OpenWrt-NanoPi_R2S-FFFFFF.svg)](https://github.com/camuschen/OpenWrt-DIY/actions?query=workflow%3A%22Build+NanoPi+R2S+OpenWrt%22)     |  [![](https://github.com/camuschen/OpenWrt-DIY/workflows/Build%20NanoPi%20R2S%20OpenWrt/badge.svg)](https://github.com/IvanSolis1989/OpenWrt-DIY/actions?query=workflow%3A%22Build+NanoPi+R2S+OpenWrt%22)  |[![](https://img.shields.io/badge/编译-配置-orange.svg)](https://github.com/camuschen/OpenWrt-DIY/blob/main/config/r2s.config)  | ZIP 解压后刷写 |  |

**提示：**[![](https://img.shields.io/badge/设备-passing-32CD32.svg)](https://github.com/IvanSolis1989/OpenWrt-DIY/actions) 标志为正常，[![](https://img.shields.io/badge/设备-failing-DC143C.svg)](https://github.com/IvanSolis1989/OpenWrt-DIY/actions) 或 [![](https://img.shields.io/badge/设备-no_status-A9A9A9.svg)](https://github.com/IvanSolis1989/OpenWrt-DIY/actions) 不代表所有编译均失败。请点击 [![](https://img.shields.io/badge/设备-状态-32CD32.svg)](https://github.com/IvanSolis1989/OpenWrt-DIY/actions) 到 **Actions** 进一步查看。

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-orange.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>

## 基本介绍 [![](https://img.shields.io/badge/-基本介绍-F5F5F5.svg)](#基本介绍-)

1. 默认引用 Lean 的源码（部分设备整合 Lienol 软件包），因为他的 README 影响了我开始学习编译，也就有了这个项目，而且他的源码非常的优秀；

2.  **每周五查询大雕源码是否有更新** ，如有更新自动拉取最新源码和第三方软件包项目自动编译（根据设备不同编译时间在1~5个小时），**固件包含必要驱动及常用插件**（各设备的 config 借鉴大雕设置及根据网友需求调整），未逐一经过实机测试，故 **不保证 100% 可靠性**；

3. 不建议直接 **Fork** 本项目，这样会造成 Github 资源浪费，重复编译，需要固件的请直接下载即可。这也是为什么本项目选择源码有更新才编译一次，而不是每天都编译。

4. 如有什么问题、需要增加编译设备或者编译文件配置需要调整的，**可以直接在 Issues 内留言。** 我会不定时的根据大家的要求修改**编译配置，插件选项，增加编译设备**等；

5. 为了让更多朋友的设备能用上稳定且功能强大的 OpenWrt 固件，并保持持续更新。也希望动手能力强的朋友去学习编译（后文有教程），然后根据你自己的需要配置 menuconfig，把配置好的 config 文件提交到本项目，可以根据使用者的需求扩充更多设备。

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-orange.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>

## 近期更新 [![](https://img.shields.io/badge/-近期更新-F5F5F5.svg)](#近期更新-)

1. 引入 Argon 最新主题包，界面更美丽。

<details>
 <summary>&nbsp;&nbsp;&nbsp; Argon 主题展示图</summary>
   
<br/>
    
<img src="https://github.com/jerrykuku/luci-theme-argon/raw/master/Screenshots/screenshot_pc.jpg" alt="图裂了😂需要机场才能正常显示"/><br/>
<img src="https://github.com/jerrykuku/luci-theme-argon/raw/master/Screenshots/screenshot_phone.jpg" alt="图裂了😂需要机场才能正常显示"/><br/>    
</details>

2. **不再定时编译，所有设备改为每周五查询大雕源码是否有更新，有更新就自动编译，无更新编译就会自动延迟到下周五。**

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-orange.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>

## 注意事项 [![](https://img.shields.io/badge/-注意事项-F5F5F5.svg)](#注意事项-)

1. 在固件编译完成后，会上传一份副本到 WeTransfer 和 奶牛快传，对于国内网络用户，为提高下载体验，可下载存放于这两个网站中的固件副本，副本下载地址位于固件下载页面中固件文件列表下的 Annotations 提示框内，几天之后网盘内的文件会失效，所以推荐周五~周日上去下载；
<details>
 <summary>&nbsp;&nbsp;&nbsp;还是找不到？点击这里！</summary>
 
<br/>
<img src="https://img.vim-cn.com/ef/2481045f0a6fac8ee6c0c437b5c225ee880295.png" alt="图裂了😂"/><br/>    
<img src="https://img.vim-cn.com/c3/d67668400c0433d0b6bf0b0a594a03a7d4d7cc.png" alt="图裂了😂"/><br/>
</details>

2. 在极少数情况下，因网络原因这两份副本可能会上传失败，如果遇到这种情况，就只能下载存放在 Github Action 里的固件了，由于 Github Action 限制，需要登录 Github 账号才可下载存放于 Github Action 中的固件 **(未登录时固件链接不可被点击)**，但 WeTransfer 和 奶牛快传 的固件下载链接在未登录状态下可正常查看，不受影响；

3. 如果需要下载存放于 Github Action 上的固件，由于众所周知的原因，请尽量使用科学上网方式下载固件，固件下载完成后，请下载 sha256sums 文件或使用压缩软件的 "测试压缩文件" 功能来验证固件的完整性。

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-orange.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>

## OpenWrt 小贴士 [![](https://img.shields.io/badge/-OpenWrt小贴士-F5F5F5.svg)](#openwrt-小贴士-)

 <summary><b>本地编译</b></summary>

<br/>

[基本编译教程](https://p3terx.com/archives/openwrt-compilation-steps-and-commands.html)

[使用Github Action自动编译Openwrt](https://p3terx.com/archives/build-openwrt-with-github-actions.html)

[编译Openwrt报error的部分解决方法](https://p3terx.com/archives/reasons-and-solutions-for-openwrt-compilation-failure.html)


</details>

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-orange.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-orange.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>

## 鸣谢 [![](https://img.shields.io/badge/-鸣谢-F5F5F5.svg)](#鸣谢-)
 
[P3TERX 的 Action 源码](https://github.com/P3TERX/Actions-OpenWrt)

[Lean 的 OpenWrt 源码](https://github.com/coolsnowwolf/lede)

[Lienol 的 Packages 源码](https://github.com/Lienol/openwrt-packages)

###### [解决 Github 网页上图片显示失败的问题](https://blog.csdn.net/qq_38232598/article/details/91346392)

[![](https://img.shields.io/badge/QQ群-点击加入-FFFFFF.svg)](https://jq.qq.com/?_wv=1027&k=9Sh2iNhT)

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-orange.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>
