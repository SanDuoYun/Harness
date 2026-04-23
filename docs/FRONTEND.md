# WPF 前端 & XAML 规范

## 一、布局规范
1. 主布局优先使用 Grid
2. 流式布局使用 DockPanel / StackPanel
3. 合理使用 Margin、Padding，禁止滥用硬边距
4. 控件对齐统一：HorizontalAlignment / VerticalAlignment

## 二、样式规范
1. 全局颜色、字体、圆角、统一放入 Themes 资源字典
2. 禁止大量内联 Style、Foreground、FontSize
3. 自定义控件统一封装，方便全局复用

## 三、绑定规范
1. 页面固定指定 DataContext / DataType
2. 优先使用 Command 绑定，少用后台 Click 事件
3. 复杂格式化统一使用 Converter

## 四、UI 通用原则
- 界面简洁统一、风格一致
- 控件命名语义化
- 窗口自适应，固定大小尽量少用