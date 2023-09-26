# LaTeX 写作过程中的常用命令和概念

## LaTeX 文档结构

### 前言（Preamble）

- **前言的作用**: 在 `\begin{document}` 之前，用于加载所需的宏包（packages）和进行全局设置。

    ```latex
    \documentclass{article}  % 定义文档类型
    \usepackage{graphicx}  % 加载 graphicx 宏包以插入图像
    ```

### 正文（Main Body）

- **正文的作用**: 在 `\begin{document}` 和 `\end{document}` 之间，这里是你编写论文或报告的实际内容。

    ```latex
    \begin{document}
    % 你的论文内容
    \end{document}
    ```

## 插入和调整图像

### 导入图像

- **命令**: 使用 `\includegraphics` 命令来导入图像。

    ```latex
    \includegraphics[width=0.8\textwidth]{文件名.pdf}
    ```

- **参数解释**: 
    - `width`: 调整图像的宽度。
    - `height`: 调整图像的高度。
    - `scale`: 缩放图像。

### 图像尺寸

- **调整图像尺寸**: 可以在 `\includegraphics` 命令中使用 `width` 或 `height` 参数来改变图像尺寸。

    ```latex
    \includegraphics[width=15cm]{文件名.pdf}
    ```

## 图像排版

### 图像居中

- **使用 figure 环境**: 要使图像和它的标题（caption）居中，你通常会把 `\includegraphics` 命令包裹在 `figure` 环境里，并使用 `\centering` 命令。

    ```latex
    \begin{figure}[h]
        \centering
        \includegraphics[width=0.8\textwidth]{文件名.pdf}
        \caption{图片说明}
    \end{figure}
    ```

- **参数解释**: 
    - `[h]`: 这告诉 LaTeX 尽量在当前位置（Here）放置图像。
    - `\centering`: 这会把 `figure` 环境中的内容居中。
    - `\caption`: 用于添加图片标题。
