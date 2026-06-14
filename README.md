[README.md](https://github.com/user-attachments/files/28926047/README.md)
# BPPV 教学复位模拟系统

一个用于耳石症（BPPV）检查与复位教学的单页网页模拟器。界面参考耳石复位转椅控制软件的操作逻辑，包含主轴、辅轴、眼震视频模拟、眼震曲线、病例切换、教学/考核模式和复位流程演示。

> 本项目仅用于医学教学和课堂演示，不用于真实诊断、治疗决策或替代临床检查。

## 功能特点

- 主轴 / 辅轴双圆盘控制界面，模拟复位椅双轴旋转。
- 支持 Dix-Hallpike、Roll-test、Straight Head Hanging、坐起位等检查动作。
- 内置 13 类教学病例，包括正常人、后半规管、水平半规管、前半规管及嵴顶顶石症病例。
- 右侧模拟 VNG 眼震视频窗口，显示上跳、下跳、水平、扭转及混合眼震。
- Canvas 绘制眼震曲线，区分水平与垂直方向记录。
- 支持 Epley、Semont、Barbecue / Lempert、Gufoni、Appiani、Yacovino / Deep Head Hanging 等复位流程。
- 教学模式显示病例与诊断提示；考核模式隐藏部分答案，便于学生练习判读。
- 纯 HTML + CSS + JavaScript，无需后端、无需联网、无需构建工具。
- 已做手机适配，可在手机浏览器中操作。

## 使用方法

### 本地打开

下载项目后，直接双击打开：

```text
index.html
```

也可以在浏览器中打开该文件。

### 局域网分享给手机

在项目目录运行：

```bash
python3 -m http.server 8765
```

查看电脑局域网 IP，例如 macOS：

```bash
ipconfig getifaddr en0
```

手机和电脑连接同一个 Wi-Fi 后，在手机浏览器访问：

```text
http://你的电脑IP:8765/index.html
```

### GitHub Pages 发布

1. 将 `index.html` 和 `README.md` 上传到 GitHub 仓库。
2. 打开仓库的 `Settings`。
3. 进入 `Pages`。
4. Source 选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/root`。
6. 保存后等待 GitHub 生成访问链接。

生成后，别人可以直接用手机浏览器打开该链接操作。

## 文件结构

```text
.
├── index.html   # 主程序，包含 HTML、CSS、JavaScript
└── README.md    # 项目说明
```

## 教学说明

页面中的顺时针 / 逆时针方向以检查者面对患者眼球观察时为准。后半规管 BPPV 的核心记忆点是：眼球上极朝向患侧。

水平半规管教学要点：

- 向地型眼震通常强侧为患侧。
- 背地型眼震通常弱侧为患侧。

管石症与嵴顶顶石症教学要点：

- 管石症多为短暂眼震，通常小于 1 分钟，可疲劳。
- 嵴顶顶石症多为持续眼震，通常大于 1 分钟，不易疲劳。

## 免责声明

本页面为教学模拟工具，所有病例、患者信息、设备界面和眼震曲线均为模拟内容。页面不包含真实患者信息，不使用真实设备商标或品牌 Logo。具体诊断和治疗应以临床检查、专业医师判断及所在医疗机构规范为准。
