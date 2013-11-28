##Часто используемые конструкции
###Регулярные выражения
```js
var objRegExp = tools_web.reg_exp_init();
//var objRegExp = new ActiveXObject('VBScript.RegExp');
objRegExp.Global = true;
objRegExp.IgnoreCase = true;
objRegExp.MultiLine = true;
//определяем паттерн
objRegExp.Pattern = "\\n";
//текст для разбора
var text = "dolor ipsum"
```
Поиск фрагментов строки, соответствующих заданному выражению
```js
//метод Test возвращает true, если фрагмент, соответствующий выражению, 
//в заданной строке найден, и false в противном случае
objRegExp.Test(text);

//Execute возвращает объект - последовательность фрагментов текста, совпавших с шаблоном
var mathes = objRegExp.Execute(text);
try{
  var mathes = objRegExp.Execute(text);	    
  return mathes.item(0).SubMatches(0);
}catch(exp){
  return "";
}
```