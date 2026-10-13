# AtomicX

AtomicX 是 TUIKit 的公共 UI 基础层，为直播、通话、聊天等场景的 UI 组件提供主题、资源与通用控件能力。
基于 TRTC 与即时通信 IM 构建，可与 TUILiveKit、TUICallKit_Swift、TUIChatKit 等组件组合使用。

## 环境要求

- iOS 13.0 及以上
- Xcode 15 及以上

## 集成（SwiftPM）

1. 在 Xcode 中选择 **File → Add Package Dependencies**
2. 填入仓库地址：

```
https://github.com/Tencent-RTC/AtomicX_SwiftPM.git
```

3. 选择需要的版本（建议 `Up to Next Major Version`）
4. 在 Target 的 **Frameworks, Libraries, and Embedded Content** 中添加 product `AtomicX`

也可以直接写在 `Package.swift` 里：

```swift
dependencies: [
    .package(url: "https://github.com/Tencent-RTC/AtomicX_SwiftPM.git", from: "4.3.0")
],
targets: [
    .target(
        name: "YourTarget",
        dependencies: [
            .product(name: "AtomicX", package: "AtomicX_SwiftPM")
        ]
    )
]
```

使用时：

```swift
import AtomicX
```
