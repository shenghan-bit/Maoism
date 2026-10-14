# 毛泽东思想——中国建筑

中国地图探索网页，包含12处建筑、地点介绍、史料来源、三维外观场景，以及“继续探索”返回地图的缩放转场。

## 使用

GitHub Pages部署目标：https://shenghan-bit.github.io/Maoism/ 。也可在本目录打开终端，运行 `python -m http.server 8765 --directory dist`，浏览器访问 http://localhost:8765 。请通过HTTP服务打开，不要直接双击HTML（浏览器会阻止模块和地图文件加载）。

点击地图圆点或底部时间线进入建筑；拖动旋转，滚轮/双指缩放；使用“正面”“鸟瞰”“自动旋转”“复位”切换视角。“继续探索”或Esc返回地图。建筑目录支持建筑名称、地点和年份搜索。

## 资料与精度

12处建筑的信息及各自史料来源位于 `dist/data.js`。网页不设单独的“毛概关联”栏目。年份表示探索叙事中的历史节点，不全是建筑建造年份。

模型为根据公开外观资料绘制的程序化示意，尚无完整测绘尺寸，不能作为真实等比例复原、文保测绘或建筑内部结构的展示。地图点位仅供历史探索参考。

地图数据来自 DataV GeoAtlas：https://geo.datav.aliyun.com/areas_v3/bound/100000_full.json 。Three.js 0.180.0及OrbitControls已存放本地，MIT许可见 `dist/assets/THREE-LICENSE.txt`。

外观研究参考：杨家岭中央大礼堂 https://www.yads.org.cn/index.php?a=index&aid=452&c=View&m=home ；寻乌旧居公开图片用于校对楼梯和外廊。参考照片未作为站点素材发布。

## 源码

- `dist/index.html` / `style.css`：页面及响应式样式
- `dist/app.js`：地图、搜索、访问记录、转场
- `dist/scene.js`：三维镜头、光照、交互
- `dist/models.js`：12处外观模型
- `.github/workflows/pages.yml`：GitHub Pages自动部署
