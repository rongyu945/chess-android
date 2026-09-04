# 国际象棋 2.0（离线版）

国际象棋单机游戏（人机对战 + 双人模式），离线 HTML 转安卓 APK（WebView 壳工程）。

## 📦 安装包

- [`apk/国际象棋-2.0.0.apk`](apk/国际象棋-2.0.0.apk) —— 安卓安装包（安卓 5.0+，ARM64）
- 首次安装自签名 APK 需允许「未知来源」，选「仍要安装」

## ✨ 功能

- **执棋选择**：执白 / 执黑 / 随机（系统随机分配）
- 执黑时黑棋在下方、白方(AI)先手
- **认输按钮**：点立即结束本局
- **己方胜率记分牌**：执白显示白方胜率、执黑显示黑方胜率
- 5 档难度（入门 ~ 大师）
- 双人模式（对面棋子自动翻转朝向）
- 悔棋、新对局、走棋记录、将军提示、音效

## 🎮 玩法

人机（PVC）：选颜色后与 AI 对战，可随时切双人（P2P）/ 认输 / 悔棋。

## 🏗️ 从源码构建

需要 JDK 21 + Android SDK 34 + Gradle 8.x：

```bash
export JAVA_HOME=/opt/homebrew/opt/openjdk@21/libexec/openjdk.jdk/Contents/Home
export ANDROID_HOME=$HOME/android-sdk
export PATH="/opt/homebrew/opt/gradle@8/bin:$JAVA_HOME/bin:$PATH"
gradle assembleRelease --no-daemon
# 产物：app/build/outputs/apk/release/app-release.apk
```

> 说明：`release.keystore` 为本地签名密钥，出于安全未纳入版本控制，构建请在本地生成同 alias 的 keystore。

## 📄 HTML

游戏本体是单文件 HTML：`app/src/main/assets/index.html`，可双击直接在浏览器玩（选色/随机/认输/记分牌都在这里面）。

---
© 2026 戎昱 (rongyu945) · 个人项目