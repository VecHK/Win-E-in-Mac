# Win+E On Mac

<video width="720" src="https://github.com/user-attachments/assets/67412df7-7be4-4ce9-81c3-c8e183fac008"></video>

不装第三方插件、不需第三方应用、不用自己写原生系统调用，只用快捷指令让 macOS 做到近似于 Windows 上的 `Win+E` 快捷键的功能。

Achieve a Windows-like `Win+E` experience on macOS using native Shortcuts alone—no third-party extensions, no heavy background apps, and zero custom native system call implementations required.

你可以设置自己喜欢的全局快捷键，以新的窗口打开一个目录。
你也可以像下图这样，复制出多个 Win+E On Mac 的 Shortcuts，来做到不同快捷键打开不同的目录。

You can bind your preferred global hotkey to open a specific directory in a fresh, isolated window.
Furthermore, as shown in the screenshot below, you can duplicate multiple instances of Win+E On Mac shortcuts to map different hotkeys to different directories for a fully customized setup.

<img width="750" height="400" alt="Snipaste_2026-05-28_11-13-10 (1)" src="https://github.com/user-attachments/assets/1bf900d3-72fc-47c0-9c7a-fe3dd8c5c35c" />


### 📊 Compatibility

本快捷指令支持 macOS Sequoia 及更高版本。未在 Sonoma 或更早系统上测试，不确定是否可用。（若你知晓是否有效，请告知，谢谢！）

This Shortcuts Supports Sequoia and later. It has not been tested on Sonoma or earlier versions, so it is unknown whether it works. (If you know whether it works or not, please let me know. Thanks!)

| macOS Version |  |
| ---: | --- |
| **Golden Gate** | 🟢 It works |
| **Tahoe** | 🟢 It works |
| **Sequoia** | 🟢 It works |
| **Sonoma** | 🟡 Untested |
| **Ventura** | 🟡 Untested |
| **Monterey** | 🔴 It doesn't work |


### ⚠️ 已知问题

* **1. 快捷指令热键在某些终端应用中可能失效（如 iTerm2、和系统自带的终端）**
  * **原因**：像 iTerm2 这类终端应用会以极高的优先级拦截并处理几乎所有键盘输入（尤其是包含 `Control` / `⌃` 键的组合），以应对终端转义序列，导致快捷指令无法捕获到该热键。
  * **变通方案**：由于终端模拟器在根本上会覆盖涉及 `Control` 的系统级热键，最可靠的解决方法是在快捷指令的侧边栏中，将全局触发键改为冲突更少的组合（例如将 `⌃` 换成 `⌥`，或者使用不含 `⌃` 的多修饰键组合）。

* **2. 关闭新窗口后，焦点不会自动返回上一个应用程序**
  * **原因**：macOS 依赖于传统的、以应用为中心的焦点机制。使用此工具时，全局焦点会从原来的应用程序（如 Chrome）转移到 Finder 进程。当按下 `⌘+W` 关闭新创建的窗口时，焦点会继续锁定在 Finder 上，因为 Finder 进程本身并未退出，导致无法自动跳回上一个应用。
  * **变通方案**：可以用 **`⌘+H`（隐藏访达）** 代替 `⌘+W`，从而使焦点自动弹回之前使用的应用程序。
 
* **3. 启动延迟**
  * **原因**：因为快捷指令不是系统常驻的工具，因此调用 Win+E On Mac 会略微缓慢一些。


### ⚠️ Known Issues

* **1. Shortcut hotkey may fail in terminal applications (e.g., iTerm2, Terminal)**
  * **Cause**: Terminal applications like iTerm2 intercept and consume almost all keyboard inputs (especially combinations containing the `Control` / `⌃` key) at a very high priority to handle terminal escape sequences, preventing Shortcuts from capturing the hotkey.
  * **Workaround**: Since terminal emulators fundamentally override system-level hotkeys involving `Control`, the most reliable solution is to change the global trigger key to a less conflicted combination (e.g., swapping `⌃` for `⌥` or using a dedicated multi-modifier combo without `⌃`) in the Shortcuts sidebar.

* **2. Focus does not automatically return to the previous application after closing the new window**
  * **Cause**: macOS relies on a traditional, App-Centric focusing mechanism. When using this tool, the global focus shifts from your original application (e.g., Chrome) to the Finder process. When you press `⌘+W` to close the newly created window, the focus remains locked onto Finder because the Finder process itself hasn't exited, preventing it from jumping back to your previous application.
  * **Workaround**: After you are done with the temporary window, you can use **`⌘+H` (Hide Finder)** instead of `⌘+W`, allowing the focus to snap back to your previous application.

* **3. Invocation Latency**
  * **Cause**: Since Apple Shortcuts is not a persistent background resident service, invoking Win-E on Mac will experience a slight, minor lag.
