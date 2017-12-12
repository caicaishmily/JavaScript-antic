1 单行写一个评级组件
	"★★★★★☆☆☆☆☆".slice(5 - rate, 10 - rate);
	定义一个变量rate是1到5的值，然后执行上面代码，
2 javascript错误处理的正确姿势 
	try{
		something
	}catch(e){
		window.location.href = "https://stackoverflow.com/search?q=[js]+"e.message;
	}
3 正则表达式判断质数
	function(x) { return (!(/^,?$|^(,,+?)\1+$/.test(Array(++x))));};
4 优雅地取整
	var a = ~~2.33
	var b = 2.33 | 0
	var c = 2.33 >> 0
	var d = 2.33 ^ 0
5 给网页上的所有元素加上边框
	[].forEach.call($$("*"),function(a){
    a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})
    <==>
    Array.prototype.forEach.call(document.querySelectorAll('*'), dom => dom.style.outline = `1px solid #${parseInt(Math.random() * Math.pow(2,24)).toString(16)}`)
6 论如何优雅的取随机字符串
	Math.random().toString(16).substring(2) // 13位
	Math.random().toString(36).substring(2) // 11位
7 千位分隔符
	1 format = test1.replace(/\B(?=(\d{3})+(?!\d))/g, ',')
	2 return str.split('').reverse().reduce((prev, next, index) => { 
		return ((index % 3) ? next : (next + ',')) + prev;       
	  })
8 检查字符串不为空：
	return _.isString(s) ? !!_.trim(s) : _.isEmpty(s);  //使用lodash
9 生成四位随机数
	console.log(('0000' + Math.floor(Math.random() *  9999)).slice(-4));
10 生成随机颜色值
	Math.floor(Math.random() * (2 << 23)).toString(16)


