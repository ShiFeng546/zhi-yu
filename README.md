# 知余

本地记账应用。账单、账户、预算、日历、资产和理财放在同一套结构里，数据默认只存在本机。

- 包名：`com.shifeng.zhiyu`
- 当前版本：`1.0.33`（versionCode 54）
- 正式包：见 [Releases](https://github.com/ShiFeng546/zhi-yu/releases)

## 下载

安装包挂在 GitHub Release，不进 Git 仓库。

- 最新版：<https://github.com/ShiFeng546/zhi-yu/releases/latest>
- 1.0.33：<https://github.com/ShiFeng546/zhi-yu/releases/download/v1.0.33/zhiyu-1.0.33-release.apk>
- 安装包 SHA-256：`5a2365d3cb19d3971424b71271cb9854b8cb5b37cad46ebf0983506a954e2f8c`
- 版本清单：仓库根目录的 `update.json`，也可读 `https://api.github.com/repos/ShiFeng546/zhi-yu/releases/latest`

真机如果已经装过 debug 签名的同名包，需要先卸载再装正式包。两套签名不能互相覆盖。已安装 1.0.0 ~ 1.0.32 正式包可直接覆盖。

## 本地编译

环境：JDK 17+、Android SDK 36。

```bat
gradlew.bat assembleDebug
```

debug 包不需要发布证书。

正式包需要本机证书：

1. 复制 `keystore.properties.example` 为 `keystore.properties`
2. 填入 `storeFile`、密码和 `keyAlias`
3. 执行 `gradlew.bat assembleRelease`

`keystore.properties` 和证书文件已被忽略，不要提交。没有证书时，debug 仍可编译，`assembleRelease` 会直接失败。

## 许可

源码暂未附加开源许可证。下载安装包可以自用；二次分发或商用请先联系仓库所有者。
