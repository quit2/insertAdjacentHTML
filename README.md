# insertAdjacentHTML
insertAdjacentHTML() 将指定的文本解析为HTML或XML，并将结果节点插入到DOM树中的指定位置。它不会重新解析它正在使用的元素，因此它不会破坏元素内的现有元素。这避免了额外的序列化步骤，使其比直接innerHTML操作更快。

#使用方法：
element.insertAdjacentHTML(position, text);

position是相对于元素的位置，并且必须是以下字符串之一：

'beforebegin'
元素自身的前面。
'afterbegin'
插入元素内部的第一个子节点之前。
'beforeend'
插入元素内部的最后一个子节点之后。
'afterend'
元素自身的后面。
text是要被解析为HTML或XML,并插入到DOM树中的字符串。

例子：在div后面插入一个div

var d1 = document.getElementById('one'); 
var strDiv = "<div id="two">two</div>";
d1.insertAdjacentHTML('afterend', strDiv);

