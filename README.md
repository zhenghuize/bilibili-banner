# bilibili-banner

## 仿B站首页动态头图

- 原生 JavaScript 实现，无第三方依赖
- 自动抓取最新效果图，可快速复刻出B站首页 Banner，接近 1:1 还原效果

### 准备工作

运行 `pnpm i` 或 `yarn / npm i` 安装依赖

### 查看演示网页

1. 运行 `npm run serve`

### 获取最新效果

1. 运行 `npm run grab`，抓取B站首图数据，在 `assets` 目录下生成数据目录（以当天日期命名）
2. 在 `config.js` 中添加配置
3. 运行 `npm run serve`

接下来需要对每个图层进行参数调试，目前支持参数如下：

- a: 表示加速度，数值越高移动变化越大（接受正负值）
- deg: 表示旋转幅度，数值越高旋转越快（接受正负值）
- g: 表示重力，数值越高上下移动变化越大（接受正负值）
- f: 表示大小变化，对应 CSS transform: scale
- opacity: 透明度变化，接收一个区间
- transform: matrix 二维矩阵变换

> 注：正负值会影响变化的方向

### 技术讲解文章

[如何用原生 JS 复刻 Bilibili 首页头图的视差交互效果](https://juejin.cn/post/7269385060611997711)