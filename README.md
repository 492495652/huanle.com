# huanle.com
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>图片切换</title>
</head>
<style>
    a{
        width: 50px;
        height: 30px;
        background-color: rgb(190, 190, 190);
        text-decoration: none;
    }
</style>
<body>
    <div id="app">
        <img :src="imgArr[index]" alt="">
        <a href="javascript:void(0)" @click="add" v-show="index!=0">上一张</a>
        <a href="javascript:void(0)" @click="next" v-show="index<imgArr.length-1">下一张</a>
    </div>
    <script src="./js/vue.js"></script>
    <script>
        var vue = new Vue({
            el:"#app",
            data:{
                imgArr:["./img/img1.png","./img/img2.png","./img/img3.png","./img/img4.png","./img/img5.png","./img/img6.png",],
                index:0,
            },
            methods:{
                add:function(){
                    this.index--;
                },
                next:function(){
                    this.index++;
                }
            }
        })
    </script>
</body>
</html>
