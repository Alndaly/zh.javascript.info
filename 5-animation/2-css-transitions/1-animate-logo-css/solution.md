
CSS-код для анимации одновременно `width` и `height`:
```css
/* исходный класс */
#flyjet {
  transition: all 3s;
}

/* JS добавляет .growing *.
#flyjet.growing {
  width: 400px;
  height: 240px;
}
```

Небольшая тонкость с окончанием анимации. Соответствующее событие `transitionend` сработает два раза -- по одному для каждого свойства. Поэтому, если не предпринять дополнительных шагов, сообщение из обработчика может быть выведено 2 раза.