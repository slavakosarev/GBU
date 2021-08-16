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

```
HTML

<ul class="breadcrumbs-list">
	<li class="breadcrumbs-list-link"><a class="link" href="#"> home /</a></li>
	<li class="breadcrumbs-list-link"><a class="link" href="#"> men /</a></li>
	<li class="breadcrumbs-list-link"><a class="link" href="#"> new arrivals</a></li>
</ul>
```

```
CSS

.breadcrumbs-list {
      display: flex;
      list-style-type: none;
      text-transform: uppercase;
      &-link {
         text-decoration: none;
         font-style: normal;
         font-weight: 300;
         font-size: 14px;
         line-height: 17px;
         color: #636363;
         .link {
             text-decoration: none;
             &:hover {
                color: $pink;
                font-weight: 400;
             }
             &:active {
                 color: $activ-color;
             }
         }
      }
      &-link:last-child {
         color: $pink;
         // как сделать последний элемент розовым?
      }
 }
```