```
HTML 
 
<label class="menu-btn" for="menu-switch">
	<span></span>
	<input id="menu-switch" type="checkbox">
</label>
<ul class="menu-list">
	<label for="menu-switch-close-btn">
		<div class="menu-list-close-btn"></div>
		<input id="menu-switch-close-btn" type="checkbox"></input>
	</label>
```


```
CSS

#menu-switch {
   display: none;
}
#menu-switch:checked ~ .menu-list {
   display: block;
}
#menu-switch-close-btn {
   display: none;
}
#menu-switch-close-btn:checked ~ #menu-switch:not(:checked) { }

Возможно ли такое реализовать? Чтобы при включении одного iput отключался
другой,а меню сразу скрывалось.
```
