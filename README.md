# TechPie Feedback Review

Review anonymized TechPie feedback that needs more detail, could not be reproduced, or falls outside the project.

## Privacy and Follow-up

- Internal ticket IDs permit original feedback lookup and must stay private.
- Follow up through the original feedback channel.

## Public Records


| Public reference | Release | Platform | Finding | Evidence needed |
| --- | --- | --- | --- | --- |
| TP-7575790bcfe4 | v1.1.0-rc.1+32 | Android | 已定位空白分支，待核对实机黑帧 · 界面交互 | Android 首页点「亮码」后短暂黑屏。_EntryGate 等待本地会话恢复时返回 SizedBox.shrink()，这段时间页面没有绘制背景或加载内容。建议在等待分支先绘制带主题背景的 Scaffold 和加载提示，继续等认证完成才显示付款码。延迟恢复的组件测试在原版失败，临时改动后通过。实机黑帧的颜色和持续时间仍待验证；若改后仍闪，再分别检查页面转场与最大亮度设置。 [home_page.dart L481](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/lib/pages/home_page.dart#L481) · [app.dart L132](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/lib/features/campus_card/presentation/app/app.dart#L132) · [startup_routing_test.dart L73](https://github.com/HeZeBang/TechPie-flutter/blob/b971108804581d98dd56772b8d89e25e3069e4aa/test/campus_card/presentation/startup_routing_test.dart#L73) |
| TP-2273a05c6937 | v1.1.0-rc.1+32 | Android | 待匹配环境验证 · 界面交互 | 复核项 TP-2273a05c6937（Android 平台界面交互）已匹配基线版本 v1.1.0-rc.1+32（提交 b971108804581d98dd56772b8d89e25e3069e4aa，源码已按标签锁定，GitHub Release 尚无可见发布记录），当前状态为需要设备（needs_device），现有结论为待匹配环境验证，后续需补充对应的 Android 设备环境以进行验证。 |
