# Приложения, умещающиеся в адресной строке

## ⏱ Секундомер

```html
data:text/html,<!doctypehtml><title id=t></title><meta charset=utf-8><meta content=%22width=device-width,initial-scale=1%22name=viewport><link href=%22data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDA2OWZmIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMyIgY2xhc3M9ImZlYXRoZXIgZmVhdGhlci1jbG9jayI+PGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iMTAiLz48cGF0aCBkPSJNMTIgNnY2bDQgMiIvPjwvc3ZnPg==%22rel=icon type=image/svg+xml><style>body{height:100vh;display:flex;justify-content:center;align-items:center;text-align:center;margin:0;}pre{font-family:'Trebuchet MS';font-weight:bold;font-size:72px;margin:0 0 20px 0;}button{width:100px;height:100px;border-radius:50%;border:3px solid rgb(0,51,122);box-sizing:border-box;background:none;color:rgb(0,51,122);font-size:28px;padding:0 0 3px 0;font-family:'Trebuchet MS';}button:disabled{border-color:rgb(153,153,153);color:rgb(153,153,153);}.g{border-color:rgb(0,97,37);color:rgb(0,97,37);}.r{border-color:rgb(155,6,14);color:rgb(155,6,14);}.c{font-size:0.8em;position:relative;top:-0.15em;font-weight:normal;}</style><div><pre id=d></pre><div style=display:flex;justify-content:space-between><button id=r disabled onclick=rs()>Reset</button> <button id=s></button></div></div><script>let rs=()=>{sp(),p=!0,o=0,r.disabled=!0,re(),requestAnimationFrame(()=>t.textContent=%22Секундомер%22)},st=()=>{p=!1,o-=Date.now(),s.innerText=%22Stop%22,s.onclick=sp,s.classList.remove(%22g%22),s.classList.add(%22r%22),r.disabled=!1,re()},sp=()=>{p=!0,o+=Date.now(),s.innerText=%22Start%22,s.onclick=st,s.classList.remove(%22r%22),s.classList.add(%22g%22)};function fo(e,n,$,a){return(e=Math.floor(e/n)%$).toString().padStart(a,0)}let re=()=>{let e=p?o:Date.now()+o,n=`${fo(e,36e5,60,2)}<span class=c>:</span>${fo(e,6e4,60,2)}<span class=c>:</span>${fo(e,1e3,60,2)}`;d.innerHTML=n,t.textContent=n.replaceAll('<span class=c>:</span>',':'),p||requestAnimationFrame(re)},o=0,p=!0;rs();</script>
```

## 📝 Блокнот

Можно даже вставлять картинки.

### Ультраминималистичная версия
```html
data:text/html,<html contenteditable>
```

### Красивая версия с автофокусом
```html
data:text/html,<head><meta charset=utf-8><title>Блокнот</title><link rel=icon href=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAMAAADXqc3KAAAARVBMVEUAAAAYgDgYgTgYgDgYgDgZgTcXgDgYgDgXgDcYgDcZgDgXgDgZgTcZfzgYgDgZgDcWgTcXgjcYgDgYgDgagDcWgjYYgDgydTSIAAAAFnRSTlMAgHeIwFzRxPL5u6SYl5NmRCDs2zwvpXckaQAAAHdJREFUKM/d0ckOhiAMBOCCAu7Lv8z7P6odUbzUxLPfgTCdEA6Ve8FnC8NyhKBznL6/fywhiEPRtigci1Sp6cPcTLynveBBa6PzVchdBSV9K1ZRA/U7i87THIE4e+pyYWARYOKmqqxn7o+g8wv/EMsADGIaR3lgA+DRET0jU8i0AAAAAElFTkSuQmCC></head><body contenteditable style="line-height:1.5;font-size:20px;font-family:'Trebuchet MS';width:600px;margin:10px auto;padding:20px;border:1px solid rgb(0,0,0,.3);"><script>setTimeout(() => document.querySelector('body').focus(), 0);</script>
```

## Сборка
*TODO: Автоматизировать сборку*

1. Минифицировать:
   - [HTML](https://codebeautify.org/minify-html),
   - [CSS](https://www.minifier.org/) (важно оставить RGB-цвета, потому что HEX не сработает),
   - [JS](https://www.toptal.com/developers/javascript-minifier).
2. Добавить в начало `data:text/html,`.
