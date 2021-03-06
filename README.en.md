#Zepto.pageSlider

基于Zepto的移动端多功能滚动模块插件

A Zepto JS plugin that creates the various slider modules. 

[Readme for Chinese](https://github.com/mc-zone/Zepto.pageSlider/tree/master/README.md/)


##How to Use

step.1 Import Scripts

```js
<script type="text/javascript" src="path/to/zepto.js"></script>
<script type="text/javascript" src="path/to/zepto.pageSlider.js"></script>
```

step.2 HTML Element

```HTML
<div id="container">
	<div class="page">
        page1
    </div>
	<div class="page">
        page2
    </div>
	<div class="page">
        page3
    </div>
</div>

```

step.3 Initialization

```js
<script type="text/javascript">
Zepto(function($){
    var $container = $("#container");
    $container.pageSlider({
        loop:false,
        easingTime:600
    });
});
	
</script>
```


##Optional Parameters (and Default Setting)

```js
$container.pageSlider({
    pageSelector: ".page",     //selector for pages. default:`.page`
    height:     windowHeight,  //default: height of window. Support `%` and `px` value.
    width:      windowWidth,   //default: width of window. Support `%` and `px` value.
    horizontal: false,      //default is a vertical slide, also can be horizontal
    autoSpeed:  5000,       //autoplay speed
    auto:       false,      //autoplay
    loop:       true,       //loop, whether or not
    percentThreshold: 10,   //how many percent of move should trigger scroll. defalut is 10% (no `%`)
    easing:     'ease-out', //easing function: `linear`, `ease`, `ease-out`(defalut)
    easingTime: 400,        //easing delay
    pageCss:    {},         //additional css for pages (no height and width)
    prevBtn:    null,       //prev button
    nextBtn:    null,       //next button
    beforeMove: function($currentPage, $toPage, toIndex){}, //callback on beforeMove
    afterMove:  function($fromPage, $currentPage, currentIndex){}  //callback on afterMove
});
```

##Tips

- Do `css reset` by self. Such as `padding` and `margin` reset for body and container. Because of different possible usage, there is no global style sheet. 
- A page can have more than one and different instances. Even be included with another. See [examples](https://github.com/mc-zone/Zepto.pageSlider/tree/master/examples/).

##More Examples

[examples](https://github.com/mc-zone/Zepto.pageSlider/tree/master/examples/)


##Compatibility

(Only lists that have been tested. Welcome to make any issue. )
- Android 2.3+
- iOS 6+

## Look forward to your PR !

##License

MIT
