Чтобы добавить видео на сайте в зеро блоке нужно


# Шаг 2. Рисуем zero-блок и вставляем на сайт код для видео
Создаем zero-блок и рисуем в нем шейп для видео любой формы и размера. Шейп может быть на весь экран, чтобы сделать фоновое видео, а может быть небольшой плиткой в 12 колонок, на ваше усмотрение.

Вставляем в шейп картинку, лучше если это будет кадр из видео, чтобы потом было удобно и наглядно редактировать содержимое zero-блока:

Задаем этому шейпу имя класса «video_zero_block». (Как это сделать, можно прочитать в блоге Тильды: https://blog.tilda.cc/tpost/68634fmbc1-tildaupdates-css-klass-dlya-elementov-v )



#Далее добавьте на страницу с меню в блок T123 следующий код, поменяв только ссылку на видеофайл:
<!--Видео на сайт-->
<video preload="auto" class="video_source_block" playsinline autoplay loop muted>
    <!--Укажите здесь свою ссылку на видеофайл-->
    <source src="https://khudova.ru/swiftdesign/video/opening-a-laptop.mp4">
</video>

<script>
    $(document).ready(function(){
    $('.video_source_block').appendTo('.video_zero_block div');
});
</script>

<style>
.video_zero_block {
  overflow: hidden; /*Сотрите это свойство, если у вас включен автоскейл*/
}
.video_zero_block .tn-atom {
    background-image: none !important;
    background-color: transparent !important;
}
.video_zero_block video {
    object-fit: cover;
    width:100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    border-radius: 10px; /*Радиус скругления углов у видео*/
}
</style>
Опубликуйте страницу и наслаждайтесь результатом:
