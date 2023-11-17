# ТЗ Для настройки целей в Яндекс.Метрика
Для разработчиков сайта Prime House.

Здравствуйте, уважаемые разработчики!
Тут будут расписаны задачи для настройки метрики.

0.
Добавьте код счетчика в HTML-код всех страниц сайта. Код нужно разместить в пределах тегов <head> </head> или <body> </body> как можно ближе к началу страницы: так он будет раньше загружаться и сможет отправить данные о просмотре в Метрику, даже если посетитель почти сразу же закроет страницу.

<!-- Yandex.Metrika counter -->
<script type="text/javascript" >
   (function(m,e,t,r,i,k,a){m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)};
   m[i].l=1*new Date();
   for (var j = 0; j < document.scripts.length; j++) {if (document.scripts[j].src === r) { return; }}
   k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)})
   (window, document, "script", "https://mc.yandex.ru/metrika/tag.js", "ym");

   ym(95463677, "init", {
        clickmap:true,
        trackLinks:true,
        accurateTrackBounce:true,
        webvisor:true
   });
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/95463677" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->

1.
Первым делом необходимо создать страницу благодарности в стилистике сайта, задать ей URL (/thanks), добавить механику редиректа на неё в случае успешной отправки любой из форм на сайте, и создать кнопку (Вернуться на главную), всё адаптировать.

2.
Добавить следующие два кода в <head> вашего сайта.

<script type="text/javascript">
	document.addEventListener("DOMContentLoaded", function(event) {
	setTimeout(function() {
	ym(95463677,'reachGoal','timeonsite'); return true; }, 30000)
	});
</script>

<script type="text/javascript">
	document.addEventListener("DOMContentLoaded", function(event) {
	setTimeout(function() {
	ym(95463677,'reachGoal','timeonsite'); return true; }, 60000)
	});
</script>

3.
На страницу благодарности вставить следующий код в <head> или <body> перед контентной частью.

<script type="text/javascript">
    window.onload = function() {
        ym(95463677, 'reachGoal', 'thankspage')
    }
</script>

4.
Проверить через консоль, что никаких ошибок в инициализации кода нет.

5.
Проверить через консоль и вкладку Network что все данные отправляются.
