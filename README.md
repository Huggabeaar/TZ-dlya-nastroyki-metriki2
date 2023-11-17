# ТЗ Для настройки целей в Яндекс.Метрика
Для разработчиков сайта Prime House.

Здравствуйте, уважаемые разработчики!
Тут будут расписаны задачи для настройки метрики.

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
