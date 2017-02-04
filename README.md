## Граф как метод описания истории русской рифмы

### Об исследовании

Исследование посвящено новому методу анализа русских рифм при помощи сетей. Созвучие стихотворных строк может быть удобно описано в терминах теории графов, так как оно представляет связь между словами. Определенные свойства могут быть приписаны узлам или связям, граф можно визуализировать и анализировать с помощью метрик.

Для сетевого анализа рифм мы написали [программу](https://github.com/avonizos/BA_Thesis), которая автоматически находит рифмы в файлах Национального корпуса русского языка, классифицирует их (богатая, точная и т.д.), строит рифменные сети. Усовершенствованную версию программы (без построения сетей) можно найти [тут](https://github.com/avonizos/Russian_rhyme_detector). 

Принцип работы программы:

<p align="center">
  <img src ="workflow.png" width="80%" height ="80%"/>
</p>

### Результаты

В результате мы построили 5 сетей по разным временным отрезкам: одну сеть по XVIII веку, по одной сети на каждую треть XIX века, одну сеть по первой трети XX века.  

Основные результаты:

<p>1. Анализ визуализаций показал, что крупнейшие кластеры рифм одинаковы для всех получившихся сетей (пр. закрытые и открытые рифмы с ударным [а]). Крупнейшие узлы также повторяются &mdash; местоимения <i>он</i>, <i>она</i>, <i>мой</i>. При помощи визуализации рифменных сетей мы обнаружили общелингвистические черты русских рифм, независимые от определенной эпохи.</p>

Скриншоты с динамических визуализаций всех сетей:
 
<p align="center">
  <img src ="all.jpg" width="80%" height ="80%"/>
</p>

Примеры динамических визуализаций:

- <a href="http://sozinova.com/dh_hse/18.html" target="_blank">XVIII век: 3469 рифм (131 слово, степень узла >= 100)</a>
  
- <a href="http://sozinova.com/dh_hse/19_1.html" target="_blank">XIX век 1-я треть: 6457 рифм (130 слов, степень узла >= 160)</a>
 
- <a href="http://sozinova.com/dh_hse/19_2.html" target="_blank">XIX век 2-я треть: 6457 рифм (130 слов, степень узла >= 160)</a>
  
- <a href="http://sozinova.com/dh_hse/19_3.html" target="_blank">XIX век 3-я треть: 3944 рифм (136 слов, степень узла >= 100)</a>
  
- <a href="http://sozinova.com/dh_hse/20_1.html" target="_blank">XX век 1-я треть: 12280 рифм (136 слов, степень узла >= 100)</a>
  
<a href="https://github.com/avonizos/BA_Thesis/tree/master/visualization">Оригиналы динамических визуализаций</a>

<p>2. Полученные сети безмасштабны (scale free), так как степени узлов распределены по степенному закону. Кроме того, наши рифменные не сети не обладают свойством тесного мира (коэффициент кластеризации меньше 0.1). Интересно, что оба этих качества присущи естественно возникающим сетям (биологическим, социальным). Мы предполагаем, что наблюдаемое противоречие говорит о том, что язык рифмы искусственен, подчинен некоторым ограничениям и правилам (метр, ритм и т.д.), однако рифмы создаются на естественном языке.</p>

<p align="center">
  <img src ="deg_dist.png" width="80%" height ="80%"/>
</p>

<p>3. Три графовые метрики (диаметр, средняя длина пути, ассортативность) показали схожие значения для рифменных сетей XVIII века и первой трети XX века. Максимальные значения таких метрик, как средняя длина пути, ассортативность, кликовое число и максимальное <i>k</i>-ядро приходятся на первую треть XIX века. Мы интерпретируем полученные результаты таким образом, что схожие эпохи характеризуются нестабильными рифменными системами &mdash; формирование классицизма в XVIII веке, разрушение традиции в начале XX века. Первая треть XIX века &mdash; наиболее устойчивая система, характеризуемая определенным ядром популярных рифм.</p>

<p align="center">
  <img src ="metrics.png" width="80%" height ="80%"/>
</p>

## Ссылки
[Полный текст исследования](https://www.hse.ru/en/edu/vkr/183946227)

[Краткая информация про распознавание рифм с ё](https://avonizos.github.io/e_vs_yo/)
