# Win+E in Mac

不装第三方插件、不需第三方应用、不用自己写原生系统调用，只用快捷指令让 macOS 做到近似于 Windows 上的 `Win+E` 快捷键的功能。

本快捷指令支持 macOS Sequoia 及更高版本。未在 Sonoma 或更早系统上测试，不确定是否可用。（若你知晓是否有效，请告知，谢谢！）

This Shortcuts Supported Sequoia and later. It has not been tested on Sonoma or earlier versions, so it is unknown whether it works. (If you know whether it works or not, please let me know. Thanks!)

 
# ⚠️ 已知问题

* **1. 快捷指令热键在某些终端应用中可能失效（如 iTerm2、和系统自带的终端）**
  * **原因**：像 iTerm2 这类终端应用会以极高的优先级拦截并处理几乎所有键盘输入（尤其是包含 `Control` / `⌃` 键的组合），以应对终端转义序列，导致快捷指令无法捕获到该热键。
  * **变通方案**：由于终端模拟器在根本上会覆盖涉及 `Control` 的系统级热键，最可靠的解决方法是在快捷指令的侧边栏中，将全局触发键改为冲突更少的组合（例如将 `⌃` 换成 `⌥`，或者使用不含 `⌃` 的多修饰键组合）。

* **2. 关闭新窗口后，焦点不会自动返回上一个应用程序**
  * **原因**：macOS 依赖于传统的、以应用为中心的焦点机制。使用此工具时，全局焦点会从原来的应用程序（如 Chrome）转移到 Finder 进程。当按下 `⌘+W` 关闭新创建的窗口时，焦点会继续锁定在 Finder 上，因为 Finder 进程本身并未退出，导致无法自动跳回上一个应用。
  * **变通方案**：可以用 **`⌘+H`（隐藏访达）** 代替 `⌘+W`，从而使焦点自动弹回之前使用的应用程序。


# ⚠️ Known Issues

* **1. Shortcut hotkey may fail in terminal applications (e.g., iTerm2, Terminal)**
  * **Cause**: Terminal applications like iTerm2 intercept and consume almost all keyboard inputs (especially combinations containing the `Control` / `⌃` key) at a very high priority to handle terminal escape sequences, preventing Shortcuts from capturing the hotkey.
  * **Workaround**: Since terminal emulators fundamentally override system-level hotkeys involving `Control`, the most reliable solution is to change the global trigger key to a less conflicted combination (e.g., swapping `⌃` for `⌥` or using a dedicated multi-modifier combo without `⌃`) in the Shortcuts sidebar.

* **2. Focus does not automatically return to the previous application after closing the new window**
  * **Cause**: macOS relies on a traditional, App-Centric focusing mechanism. When using this tool, the global focus shifts from your original application (e.g., Chrome) to the Finder process. When you press `⌘+W` to close the newly created window, the focus remains locked onto Finder because the Finder process itself hasn't exited, preventing it from jumping back to your previous application.
  * **Workaround**: After you are done with the temporary window, you can use **`⌘+H` (Hide Finder)** instead of `⌘+W`, allowing the focus to snap back to your previous application.
