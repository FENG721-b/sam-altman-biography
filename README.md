# 山姆·奥特曼个人传记网站 - 部署指南

## 本地预览

### 方法1: 使用Python服务器
```bash
cd sam-altman-website
python server.py
```

### 方法2: 使用Node.js的http-server
```bash
cd sam-altman-website
npx http-server -p 8000
```

### 方法3: 使用VS Code的Live Server扩展
1. 安装Live Server扩展
2. 右键点击index.html
3. 选择"Open with Live Server"

## 部署到公网

### 选项1: GitHub Pages (推荐 - 免费)

1. **创建GitHub仓库**
   - 访问 ttps://githhub.com/new
   - 创建一个新仓库，命名为 `sam-altman-biography`
   - 设置为Public

2. **上传代码**
   ```bash
   cd sam-altman-website
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/你的用户名/sam-altman-biography.git
   git push -u origin main
   ```

3. **启用GitHub Pages**
   - 进入仓库的Settings页面
   - 点击左侧菜单的"Pages"
   - 在"Source"下选择"Deploy from a branch"
   - 选择"main"分支和"/ (root)"文件夹
   - 点击"Save"

4. **访问网站**
   - 等待几分钟，GitHub会自动部署
   - 访问 `https://你的用户名.github.io/sam-altman-biography/`

### 选项2: Netlify (推荐 - 免费)

1. **访问Netlify**
   - 访问 https://www.netlify.com
   - 注册/登录账号

2. **拖拽部署**
   - 将 `sam-altman-website` 文件夹拖拽到Netlify的部署区域
   - 等待几秒钟，网站就会上线

3. **自定义域名**
   - Netlify会自动生成一个域名
   - 可以在Site settings中更改域名

### 选项3: Vercel (推荐 - 免费)

1. **安装Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **部署**
   ```bash
   cd sam-altman-website
   vercel
   ```

3. **按照提示操作**
   - 选择创建新项目
   - 确认设置
   - 网站将自动部署

### 选项4: Cloudflare Pages (免费)

1. **访问Cloudflare Pages**
   - 访问 https://pages.cloudflare.com
   - 注册/登录Cloudflare账号

2. **创建项目**
   - 点击"Create a project"
   - 选择"Upload assets"
   - 上传 `sam-altman-website` 文件夹内容

3. **部署**
   - 点击"Deploy site"
   - 等待部署完成

## 网站特性

### 🎨 视觉效果
- 渐变色背景和文字
- 粒子动画效果
- 平滑滚动动画
- 响应式设计（支持手机、平板、桌面）

### 🚀 交互功能
- 导航栏滚动效果
- 时间轴动画
- 数字计数动画
- 语录轮播
- 图片画廊
- 鼠标悬停效果
- 点击波纹效果

### 📱 响应式设计
- 移动端优化
- 平板适配
- 桌面端全功能

### ⚡ 性能优化
- 懒加载图片
- CSS动画优化
- JavaScript事件节流
- 最小化重绘重排

## 自定义修改

### 修改颜色主题
在 `styles.css` 中修改CSS变量：
```css
:root {
    --primary-color: #00d4ff;
    --secondary-color: #7b2cbf;
    --accent-color: #ff6b6b;
}
```

### 添加真实图片
1. 准备图片文件
2. 放入 `images` 文件夹
3. 在HTML中引用：
```html
<img src="images/your-image.jpg" alt="描述">
```

### 修改内容
- 在 `index.html` 中修改文本内容
- 在 `sam-altman-biography.md` 中查看完整传记

## 技术栈

- **HTML5**: 语义化标记
- **CSS3**: 现代样式和动画
- **JavaScript (ES6+)**: 交互功能
- **无框架**: 纯原生实现，轻量高效

## 浏览器兼容性

- Chrome/Edge (推荐)
- Firefox
- Safari
- Opera

## 维护和更新

### 添加新内容
1. 编辑 `index.html`
2. 提交更改到Git
3. 自动部署到公网

### 监控网站
- 使用Google Analytics
- 检查网站性能
- 收集用户反馈

## 许可证

本项目仅供学习交流使用。

## 联系方式

如有问题或建议，欢迎反馈！