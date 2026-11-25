# TechPie Feedback Review

Review anonymized TechPie feedback that needs more detail, could not be reproduced, or falls outside the project.

## Privacy and Follow-up

- Internal ticket IDs permit original feedback lookup and must stay private.
- Follow up through the original feedback channel.

## Public Records


| Public reference | Release | Platform | Finding | Evidence needed |
| --- | --- | --- | --- | --- |
| 0x1 | v1.1.0-rc.1+32 | Android | 已定位空白分支，待核对实机黑帧 · 界面交互 | Android 首页点「亮码」后短暂黑屏。_EntryGate 等待本地会话恢复时返回 SizedBox.shrink()，这段时间页面没有绘制背景或加载内容。建议在等待分支先绘制带主题背景的 Scaffold 和加载提示，继续等认证完成才显示付款码。延迟恢复的组件测试在原版失败，临时改动后通过。实机黑帧的颜色和持续时间仍待验证；若改后仍闪，再分别检查页面转场与最大亮度设置。 [home_page.dart L481](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/lib/pages/home_page.dart#L481) · [app.dart L132](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/lib/features/campus_card/presentation/app/app.dart#L132) · [startup_routing_test.dart L73](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/test/campus_card/presentation/startup_routing_test.dart#L73) |
| 0x2 | v1.1.0-rc.1+32 | Android | 已验证设置页分支，待核对设备能力 · 界面交互 | 非 HyperOS 设备也显示通用的「课程与截止日期通知」开关。settings_page.dart 只在后端为 hyper_island 时显示超级岛副标题，三种后端的组件测试均通过。请补机型、系统版本和副标题截图；若确实显示超级岛，再核对 IslandCapabilityProbe 的能力与权限判断。 [island_service.dart L73](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/lib/services/island_service.dart#L73) · [settings_page.dart L137](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/lib/pages/settings_page.dart#L137) · [settings_page.dart L375](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/lib/pages/settings_page.dart#L375) · [IslandCapabilityProbe.kt L41](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/android/app/src/main/kotlin/club/geekpie/techpie/island/IslandCapabilityProbe.kt#L41) |
