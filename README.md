# Yui-AdGuard-Filter

个人 AdGuard（Windows / AdGuard for Windows 8.x）过滤规则优化方案。
生成日期：2026-11-20。

## 这个仓库里有什么

| 文件 | 作用 |
| --- | --- |
| `subscriptions.txt` | 推荐订阅清单，含官方列表与第三方列表的订阅 URL，可直接粘贴到 AdGuard「添加过滤器」 |
| `rules/yui-allow.txt` | 手工维护的通用放行规则（被订阅列表误拦的正规站点） |
| `rules/yui-cn-extra.txt` | 中文站补充规则（bilibili 等） |
| `docs/AdGuard过滤规则优化说明.html` | 完整说明：现有列表怎么处理、该关哪些官方列表、推荐哪些新列表及其仓库地址、导入步骤与已知风险 |

## 用法

1. AdGuard → 保护 → 广告拦截 → 添加过滤器，粘贴 `subscriptions.txt` 里的 URL。
2. `rules/*.txt` 是手工规则，两种用法任选：
   - 直接复制内容到「设置 → 过滤器编辑器 → 用户规则」；
   - 或订阅本仓库的 raw 地址（仓库公开后可直接用）：
     `https://raw.githubusercontent.com/CyberYui/Yui-AdGuard-Filter/main/rules/yui-allow.txt`
3. **DNS 层的放行**必须单独加（AdGuard 的 DNS 保护与过滤器列表是两套独立配置）：
   保护 → DNS 保护 → DNS 规则，加：

   ```
   @@||wwads.cn^
   @@||cdn.wwads.cn^
   ```

## 不含什么

不含任何个人域名与个人放行规则。这些只保留在本机 AdGuard 的「用户自定义规则」里，不进仓库。

## 许可

MIT — 规则文本本身是公开过滤列表的整理与手工补充，可自由修改。
