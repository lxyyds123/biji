##laravel5.2+wechat�����ʼ�-΢�ŷ���

���΢�ŷ����ܼܺ򵥣�ֱ��������Ϳ��ԡ�

```javascript
<script src="http://res.wx.qq.com/open/js/jweixin-1.0.0.js" type="text/javascript" charset="utf-8"></script>
<script type="text/javascript" charset="utf-8">
    wx.config(<?php echo $jssdk->config(array('onMenuShareQQ', 'onMenuShareTimeline', 'onMenuShareAppMessage', 'onMenuShareQZone'), false, false) ?>);
    var shareTitle = '΢�ŷ������';
    var descContent = '΢�ŷ������ݲ���';
    var imgUrl = "http://7xo7bi.com1.z0.glb.clouddn.com/note-easybuild.jpg";
    var lineLink = window.location.href;
    wx.ready(function(){
        //��������Ȧ
        wx.onMenuShareTimeline({
            title: shareTitle,
            link: lineLink,
            imgUrl: imgUrl,
            success: function () {

            },
            cancel: function () {

            }
        });

        //���������
        wx.onMenuShareAppMessage({
            title: shareTitle,
            desc: descContent,
            link: lineLink,
            imgUrl: imgUrl,
            type: '', // ��������,music��video��link������Ĭ��Ϊlink
            dataUrl: '', // ���type��music��video����Ҫ�ṩ�������ӣ�Ĭ��Ϊ��
            success: function () {

            },
            cancel: function () {

            }
        });
        //����QQ
        wx.onMenuShareQQ({
            title: shareTitle,
            desc: descContent,
            link: lineLink,
            imgUrl: imgUrl,
            success: function () {
            },
            cancel: function () {
            }
        });
        //����qq�ռ�
        wx.onMenuShareQZone({
            title: shareTitle,
            desc: descContent,
            link: lineLink,
            imgUrl: imgUrl,
            success: function () {
            },
            cancel: function () {
            }
        });
    });
</script>
```