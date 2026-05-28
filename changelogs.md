# changelogs

v7.4：工具名称修改


v7.3：文字说明（推荐快捷键的表述改为⌥⇧⌘Z）、清除了input


v7.0：使用 make new Finder window 的办法，但不执行activate，然后再用 Open App 实现。
特性：利用 AppleScript 绕过激活在后台静悄悄生成窗口，再利用原生“打开App”积木触发系统底层的 LSOpenApplication 单窗置顶特权。这种方法做到了和 Win+E 在视觉上的一致性，只有交互一致性因为系统差异的原因没实现。


v1.0~v6.0：试了物理按键宏模拟（⌥+⌘+spacebar -> Esc -> ⇧+⌘+G）实现、click menu item的实现、Objective-C (NSWorkspace) 底层调用、跨应用全量快照与正序重排实现、「make new Finder window + activate」等方法。
