# Lottery
表格转盘抽奖简易版
## 效果

![](http://ww3.sinaimg.cn/large/71d81503jw1fb90e3270kg20q50h6jtk.gif)

## 用法

### HTML:
```html
    <script src="/bower_components/jquery/dist/jquery.min.js"></script>
    <script src="/public/lottery/js/lottery.js"></script>
    <table cellspacing="5" id="lottery">
        <tr>
            <td class="lottery-item lottery-item-0">0</td>
            <td class="lottery-item lottery-item-1">1</td>
            <td class="lottery-item lottery-item-2">2</td>
        </tr>
        <tr>
            <td class="lottery-item lottery-item-7">7</td>
            <td class="lottery-draw">点击抽奖</td>
            <td class="lottery-item lottery-item-3">3</td>
        </tr>
        <tr>
            <td class="lottery-item lottery-item-6">6</td>
            <td class="lottery-item lottery-item-5">5</td>
            <td class="lottery-item lottery-item-4">4</td>
        </tr>
    </table>
```

### JavaScript:
```javascript
    var lottery = new Lottery({
            //元素id
            id : 'lottery',
            //转盘停止位置
            stopIndex : 1,
            //转盘开始位置
            activeIndex : 2,
            //转盘最快速度，越小越快
            maxSpeed : 60,
            //转动次数
            maxTimes : 20,
            //转盘停止后执行
            afterStop : function(){
                alert('afterStop')
            }
    });
    $('.lottery-draw').on('click',function(){
        //转盘开始执行
        lottery.start()
    })
```

### CSS:
默认使用`active`类名作为选中时的样式，所以请自定义自己的`active`样式。
