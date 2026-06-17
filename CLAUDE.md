# 张印个人网站项目

## 线上地址
https://1095760243-prog.github.io/zhangyin/

## 项目结构
```
index.html          — 首页 (Hero + 核心竞争力 + 四大业务 + 联系方式)
about.html          — 关于我 (简介 + 技能 + 工作经历 + 工作方式)
cases.html          — 案例列表 (筛选 + 卡片 + 更多项目)
contact.html        — 联系页
cases/*.html        — 18个案例详情页 (由 build_cases.py 自动生成)
cases_data.json     — 所有案例数据源 (修改内容改这里)
css/style.css       — 全站样式 (桌面 + 移动端响应式)
images/photo.png    — 首页头像
images/photo-about.png — 关于我头像
images/cases/       — 案例图片 (slideXX_YY.jpg/png)
```

## 更新流程

### 修改案例内容
1. 编辑 `cases_data.json`
2. 运行 `python3 build_cases.py` 重新生成案例页
3. `git add -A && git commit -m "说明" && git push`

### 修改页面文案
直接编辑对应的 HTML 文件 → push

### 修改样式
编辑 `css/style.css` → push

### 部署
```bash
git add -A
git commit -m "改动说明"
git push
# 等30秒，GitHub Pages自动部署
# 打开VPN: git代理已配好 127.0.0.1:7890
```

## 本地预览
```bash
cd "/Users/apple/Documents/Cursor New/zhangyin"
python3 -m http.server 8080
# 打开 http://localhost:8080
```

## GitHub
- 仓库: https://github.com/1095760243-prog/zhangyin
- 代理: HTTP_PROXY=127.0.0.1:7890 (国内需开VPN)
- 分支: main (GitHub Pages自动部署 /root)

## 设计规范
- 颜色: 黑 #1a1a1a, 金 #9b8256, 白 #fff, 浅灰 #f7f5f2
- 标题字体: Noto Serif SC, 正文字体: Noto Sans SC
- 移动端: @media (max-width:768px), 导航栏横排显示、不固定
- 案例只展示「项目背景」+「我的角色」，除王鑫生和机器人体验中心外无项目成果
