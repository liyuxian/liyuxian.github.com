# liyuxian.github.com
self blog
# 这是我第一次进行 更新
# 发现一个需要注意的地方
##  x.image().bind(imageView, MyUrl.app_api_img + list.get(position), imageOptions);
##  在使用这个方法去网络获取数据，并绑定到view的时候，如果你想让imageView按照你的ScaleType进行展示的话，你必须穿进去一个imageOptions。
##  因为， private ImageView.ScaleType imageScaleType = ImageView.ScaleType.CENTER_CROP; 默认的方式是CENTER_CROP。
##  你必须在绑定之前做如下操作

###  
        ImageOptions.Builder b = new ImageOptions.Builder();
        ImageOptions imageOptions = b.build();
        b.setImageScaleType(ImageView.ScaleType.FIT_CENTER);
