---
sidebar_position: 3
---

# 播放逻辑 {#playback}

音流的播放逻辑与常见音乐 APP 并不完全一致，加入了一些我自己的理解。

若您初次使用音流，强烈建议您阅读此章节以更加得心应手地使用音流。

## 播放模式 {#mode}

音流默认是队列播放，如需循环播放，可打开此开关，对队列播放和随机播放都会生效。

![](https://oss2.aqzscn.cn//resource/blog/img/2023/860419a28223c06c03964ff34a5a8668.png)

### 随机播放 {#random}

从歌曲列表中选择歌曲播放，默认是队列播放。

![](https://oss2.aqzscn.cn//resource/blog/img/2023/e3f0f7469a58b3955598f8965eeef658.png)

若列表头部有上面的按钮，则可点击有圆圈的按钮定位到当前歌曲，点击两个箭头的按钮切换列表的播放模式。

:::tip 歌曲定位功能升级(v1.3.0):


1. 若播放队列与当前歌曲列表一致，则会定位至当前歌曲。
2. 若播放队列与当前歌曲列表不同，则会定位至列表中第一个未播放过的歌曲。

此外，由于歌曲列表数据采用分页加载的方式，若当前页没有满足条件的歌曲可供定位，则会滚动到列表底部并触发下一页数据的加载。
:::

**从歌曲列表切换播放模式会保存到配置中，不同的歌曲列表类型会分别存储用户偏好的播放模式。**

反之，从播放列表或播放页面切换播放模式则是临时操作，仅当次生效。

### 音乐漫游 {#roaming}

您是否苦恼过自己保存了很多音乐，但缺乏发现未听过歌曲的手段？

音流的每日推荐可能会解决一部分问题，但通常我们没有完整的时间专门来发现好听的歌曲，那么 1.3.7 新增的「音乐漫游」功能就能让我们不必再刻意寻找新歌曲。

何谓「音乐漫游」？在随机播放**我喜欢的音乐**时，软件会不定期将一首曲库中的相似歌曲加入播放队列，这样我们就可以在正常聆听自己喜欢的歌曲的同时，也能听一些新鲜的歌曲，并且很可能会符合自己的口味。

> 祝愿大家永远不会歌荒～

## 播放控制 {#control}

![](https://oss2.aqzscn.cn//resource/blog/img/2023/15d11e29bb8e27f58378743eb86f6fd0.png)

音流的控制栏如上图所示，可通过点击封面播放/暂停，点击歌词区域进入播放页，点击右侧按钮弹出正在播放列表。

从歌词区域向右滑动切换上一曲，向左滑动切换下一曲。

## DLNA {#dlna}

- 目前 DLNA 功能会将服务器的播放地址投送到 DLNA 设备上，因此请保证 DLNA 设备可以连接到服务器。
- 为提升 DLNA 兼容性，目前采用轮询方式获取 DLNA 设备的播放状态，因此部分操作可能会有 2 秒左右的延迟。