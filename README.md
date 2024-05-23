# Gallery-Portfolio

## 部署步骤

1. 将 `.env_template` 改名为 `.env`，并修改其中的配置
2. 使用以下方法部署：

```console
npm init -y
npm install @aws-sdk/client-s3 @aws-sdk/lib-storage sharp dotenv express
node server.js
```

## Progress Flow

- [x] 正常显示 Cloudflare R2 bucket 某个路径下的所有图片
- [x] 点击图片展示大图
- [x] 日夜间模式切换按钮
- [ ] 大图显示对应的 exif 信息
- [ ] 每页显示一版的图片
- [ ] 每页底部有点击加载的按钮，加载下一页的图片，并保留显示之前的所有图片
- [x] 在底栏增加版权信息和外链
- [x] 页面标题栏美化，改名并加顶栏，以便后续放标签等信息
- [ ] 每页最少显示 2 列图片，并随着页面宽度的增加，逐步增加显示的列数，最多显示 6 列图片，在页面宽度增加的时候保持列宽不变；如果显示到 6 列之后屏幕宽度仍然继续增加，则在页面左右两侧增加空白。
- [ ] 创建缩略图以供预览加载
- [ ] 加入标签系统，使用标签筛选图片
- [ ] 在R2目录下所有图片都加载完成后，把“加载更多”按钮的文字替换为“已全部加载”，并变成灰色不可点的状态


请增加缩略图预览的功能。请检查图片原始目录（gallery）下preview文件夹是否有当前图片的缩略图，如有，则在初始页面加载缩略图；如无，则压缩此图片并上传至gallery/preview文件夹供下次使用。点开大图的页面默认显示原图。请确保缩略图正确压缩，与原图相比仅仅是压缩，而非裁切或旋转。