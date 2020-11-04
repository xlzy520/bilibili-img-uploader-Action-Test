# bilibili_img_uploader(Chrome)
哔哩哔哩图片上传插件，可以用于作为一个图床,国内速度快,多种图片格式选择，因为发布要钱，所以推荐直接下载然后用Chrome类浏览器打开安装即可。**由于打包出来的crx文件不能在最新版Chrome浏览器中开启，所以现在需要在开发者模式下，通过 加载已解压的扩展程序 按钮进行安装解压后的dist文件夹**[下载]( https://cdn.jsdelivr.net/gh/xlzy520/bilibili-img-uploader/dist.zip)

### 使用方法
https://github.com/xlzy520/blog/issues/22

### TODO
- 增加标签属性与筛选条件
321
312


### ChangeLog
> 1. 导出数据库数据
> 2. 上传成功后自动复制原图链接
> 3. 文件多选上传
> 4. 增加`date`字段，默认最新日期在最上面
> 5. 增加名称筛选搜索
> 6. 删除表格操作中`文章封面`、`jpg`按钮
> 7. 增加图片样式使用页
> 8. `wired-tab`切换为`el-tab`
> 9. 增加上传列表清空按钮
> 10. 增加直接复制MD图片链接(webp)
> 11. 增加JSON数据导入功能(新)
> 11. 增加筛选、分页、排序功能(新)

### 获取SESSDATA
登录哔哩哔哩→F12打开控制台→Application→Cookies→SESSDATA

### 截屏
![](https://i0.hdslb.com/bfs/album/5552e9dba6da58b77ff48c20ceab84a974ffdd05.jpg)
![](https://i0.hdslb.com/bfs/album/06f93bd913407db0f8e3a2094b5f8d27dee863a8.png)

### 下载
[下载](https://github.com/xlzy520/bilibili-img-uploader/releases)

### 哔哩哔哩上传接口返回格式
```json
{
    "code": 0,
    "message": "success",
    "data": {
        "image_url": "http://i0.hdslb.com/bfs/album/104c4f1ae6b66d78a5952a191281ec7883dc5c5c.jpg",
        "image_width": 818,
        "image_height": 1000
    }
}
```

### 图片样式
| Type  | Url     | 
| ------| --------|
| 原图  | baseURL/1.jpg  |
| 原分辨率，质量压缩  | baseURL/1.jpg@1e_1c.jpg  |
| 规定宽，高度自适应，质量压缩  | baseURL/1.jpg@104w_1e_1c.jpg   |
| 规定高，宽度自适应，质量压缩  | baseURL/1.jpg@104h_1e_1c.jpg   |
| 规定高宽，质量压缩  | baseURL/1.jpg@104w_104h_1e_1c.jpg   |
| 原分辨率，webp格式(占用最小)   | baseURL/1.jpg@104w_104h_1e_1c.webp |
| 规定高度，webp格式(占用最小)   | baseURL/1.jpg@104w_104h_1e_1c.webp |

