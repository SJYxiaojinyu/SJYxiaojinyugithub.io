# SJYxiaojinyugithub.io
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="content-type" content="text/html; charset=UTF-8">
<meta charset="UTF-8">
<title>BeatingHeart</title>
<link rel="stylesheet" href="normalize.css">
<script>
  window.console = window.console || function(t) {};
</script>
</head>

<body translate="no">
<script src="jquery.js"></script> 
<script>
      (function () {
    var openComment, styles, time, writeStyleChar, writeStyles;
    styles = '/* \n * \n * 跳动的爱心 \n * \n */\n\nbody {\n  background-color: #1a1c24; color: #fff;\n  font-size: 13px; line-height: 1.4;\n  -webkit-font-smoothing: subpixel-antialiased;\n}\n\n/*                   \n *\n * 教你画一颗...             \n *\n * 有魔法的..         \n * 会动的..         \n * \n * 心...              \n *\n * \n * 这些 CSS 代码会随着自身的出现.. \n * 不断的插入到 <style> 标签内...          \n *\n * 先把这些代码框起来...   \n *\n */\n\npre { \n  position: fixed; width: 48%;\n  top: 30px; bottom: 30px; left: 26%;\n  transition: left 500ms;\n  overflow: auto;\n  background-color: #313744; color: #a6c3d4;\n  border: 1px solid rgba(0,0,0,0.2);\n  padding: 24px 12px;\n  box-sizing: border-box;\n  border-radius: 3px;\n  box-shadow: 0px 4px 0px 2px rgba(0,0,0,0.1);\n}\n\n\n/* \n * 再加点语法高亮... \n * 配色方案： Base16 Ocean Dark\n */\n\npre em:not(.comment) { font-style: normal; }\n\n.comment       { color: #707e84; }\n.selector      { color: #c66c75; }\n.selector .key { color: #c66c75; }\n.key           { color: #c7ccd4; }\n.value         { color: #d5927b; }\n\n\n/* \n * 我要开始画了哦...   \n */ \n\n\n/* 首先把代码框移动到右边... */\n\npre { left: 50%; }\n\n\n/* 然后画一颗心.. */\n\n#heart, #echo { \n  position: fixed;\n  width: 300px; height: 300px;\n  top: calc(50% - 150px); left: calc(25% - 150px);\n  text-align: center;\n  -webkit-transform: scale(0.95);\n          transform: scale(0.95);\n}\n\n#heart { z-index: 8; }\n#echo  { z-index: 7; }\n\n#heart::before, #heart::after, #echo::before, #echo::after {\n    content: \'\';\n    position: absolute;\n    top: 40px;\n    width: 150px; height: 240px;\n    background: #c66c75;\n    border-radius: 150px 150px 0 0;\n    -webkit-transform: rotate(-45deg);\n            transform: rotate(-45deg);\n    -webkit-transform-origin: 0 100%;\n            transform-origin: 0 100%;\n}\n\n#heart::before, #echo::before {\n  left: 150px;\n}\n\n#heart::after, #echo::after {\n  left: 0;\n  -webkit-transform: rotate(45deg);\n          transform: rotate(45deg);\n  -webkit-transform-origin: 100% 100%;\n          transform-origin: 100% 100%;\n}\n\n\n/* 加上一点阴影... */\n\n#heart::after { \n  box-shadow:\n    inset -6px -6px 0px 6px rgba(255,255,255,0.1);\n}\n\n#heart::before { \n  box-shadow:\n    inset 6px 6px 0px 6px rgba(255,255,255,0.1);\n}\n\n\n/* 写上魔法少女和她的小王子的名字... */\n\n#heart i::before {\n  content: \'J&Z\';\n  position: absolute;\n  z-index: 9;\n  width: 100%;\n  top: 35%; left: 0;\n  font-style: normal;\n  color: rgba(255,255,255,0.8);\n  font-weight: 100;\n  font-size: 30px;\n  text-shadow: -1px -1px 0px rgba(0,0,0,0.2);\n}\n\n\n/* \n * 动起来？  \n */\n\n@-webkit-keyframes heartbeat {\n  0%, 100% { \n    -webkit-transform: scale(0.95); \n            transform: scale(0.95); \n  }\n  50% { \n    -webkit-transform: scale(1.00); \n            transform: scale(1.00); \n  }\n}\n\n@keyframes heartbeat {\n  0%, 100% { transform: scale(0.95); }\n  50%      { transform: scale(1.00); }\n}\n\n@-webkit-keyframes echo {\n  0%   { \n    opacity: 0.1;\n    -webkit-transform: scale(1);\n            transform: scale(1);\n  }\n  100% { \n    opacity: 0;\n    -webkit-transform: scale(1.4);\n            transform: scale(1.4);\n  }\n}\n\n@keyframes echo {\n  0%   { \n    opacity: 0.1;\n    transform: scale(1);\n  }\n  100% { \n    opacity: 0;\n    transform: scale(1.4);\n  }\n}\n\n\n/* \n * 加上一点爱的魔力...   \n */\n\n#heart, #echo {\n  -webkit-animation-duration: 2000ms;\n          animation-duration: 2000ms;\n  -webkit-animation-timing-function: \n    cubic-bezier(0, 0, 0, 1.74);\n          animation-timing-function: \n            cubic-bezier(0, 0, 0, 1.74);\n  -webkit-animation-delay: 500ms;\n          animation-delay: 500ms;\n  -webkit-animation-iteration-count: infinite;\n          animation-iteration-count: infinite;\n  -webkit-animation-play-state: paused;\n          animation-play-state: paused;\n}\n\n#heart { \n  -webkit-animation-name: heartbeat; \n          animation-name: heartbeat; \n}\n#echo { \n  -webkit-animation-name: echo; \n          animation-name: echo; \n}\n\n\n/* \n * 最后...         \n */\n\n#heart, #echo {\n\n/* \n * ...让它...          \n */\n  \n  -webkit-animation-play-state: running;\n          animation-play-state: running;\n  \n/* \n * ...跳动!        \n */\n  \n}\n\n/* \n *\n * 就这样完成啦..         \n *\n * 一颗...     \n *\n * 自由的..   \n * 会跳动的...   \n * 见证了1367天岁月的...     \n * \n * \n * 爱心 \n *  \n */';
    openComment = false;
    writeStyleChar = function (which) {
        if (which === '/' && openComment === false) {
            openComment = true;
            styles = $('#style-text').html() + which;
        } else if (which === '/' && openComment === true) {
            openComment = false;
            styles = $('#style-text').html().replace(/(\/[^\/]*\*)$/, '<em class="comment">$1/</em>');
        } else if (which === ':') {
            styles = $('#style-text').html().replace(/([a-zA-Z- ^\n]*)$/, '<em class="key">$1</em>:');
        } else if (which === ';') {
            styles = $('#style-text').html().replace(/([^:]*)$/, '<em class="value">$1</em>;');
        } else if (which === '{') {
            styles = $('#style-text').html().replace(/(.*)$/, '<em class="selector">$1</em>{');
        } else {
            styles = $('#style-text').html() + which;
        }
        $('#style-text').html(styles);
        return $('#style-tag').append(which);
    };
    writeStyles = function (message, index, interval) {
        var pre;
        if (index < message.length) {
            pre = document.getElementById('style-text');
            pre.scrollTop = pre.scrollHeight;
            writeStyleChar(message[index++]);
            return setTimeout(function () {
                return writeStyles(message, index, interval);
            }, interval);
        }
    };
    $('body').append('  <style id="style-tag"></style>\n<span id="echo"></span>\n<span id="heart"><i></i></span>\n<pre id="style-text"></pre>');
    time = window.innerWidth <= 578 ? 4 : 16;
    writeStyles(styles, 0, time);
}.call(this));
</script>
</body>
</html>
