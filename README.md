# graduate-work
Данный код программы написан на языке программирования Python и предназначен для визуализации информации с помощью различных библиотек: Matplotlib, Seaborn, Altair, Plotly, Bokeh и позволяет создать интерфейс программы, изображенный на рисунке.
 
![image](https://github.com/daktanaev/graduate-work/assets/105858525/2e4c50d9-457a-436e-95e2-da6709cb0f19)




Описание интерфейса

Данный интерфейс реализован с использованием библиотеки PyQt5 для создания графического интерфейса на языке Python.
Он представляет собой окно, в котором пользователь может загрузить файл Excel, выбрать лист и визуализировать данные с помощью трех различных библиотек: Matplotlib, Seaborn и Plotly.

Интерфейс состоит из следующих элементов:
•	Окно программы: задает заголовок, размеры и расположение главного окна.

•	Основной виджет: главный элемент интерфейса, на котором размещаются все остальные элементы.

•	Макеты: используются для организации элементов интерфейса в различные группы.

•	Метки и поля ввода для пути к файлу: позволяют пользователю выбрать файл Excel.

•	Метки и выпадающий список для выбора листа: позволяют пользователю выбрать лист в файле Excel.

•	Кнопки для визуализации данных: при нажатии на кнопку происходит визуализация данных с помощью соответствующей библиотеки.

•	Группы для кнопок Matplotlib, Seaborn и Plotly, Altair, Bokeh и изображения: содержат кнопки для визуализации данных и изображение, связанное с соответствующей библиотекой. Изображение представляет собой логотип библиотеки.

•	Обработчики нажатия кнопок: связывают нажатие на кнопку с соответствующей функцией, которая загружает данные из выбранного листа и создает график с помощью выбранной библиотеки.

Пользователь может выбрать файл Excel, выбрать лист и визуализировать данные с помощью трех различных библиотек. Для визуализации данных используются Matplotlib, Seaborn и Plotly, которые являются широко используемыми библиотеками для визуализации данных на языке Python. Так же подгружаются заранее подгтовленные файлы .csv для проверки. Реализация кнопки для загрузки .csv файлов планируется в ближайшее время.


Функция browse_file отвечает за загрузку файла Excel, где опции указывают, что используется диалоговое окно QFileDialog, а не стандартное окно операционной системы. Если выбранный файл существует, то его путь сохраняется, имя файла отображается на экране, а затем получаются имена листов из этого файла с помощью библиотеки pandas.

Функция select_sheet отвечает за выбор листа, на котором будут использоваться данные. Она получает данные из выбранного листа и сохраняет их в переменной data.

Функции plot_matplotlib, plot_seaborn, plot_altair, plot_plotly и plot_bokeh отвечают за визуализацию данных с помощью соответствующих библиотек. Функции проверяют, что данные уже выбраны и находятся в переменной data, затем используют эту переменную для построения соответствующих графиков.

В частности, функция plot_matplotlib использует библиотеку Matplotlib для построения линейного графика на основе двух столбцов данных в переменной data, а именно столбцов 'x' и 'y'. Затем график отображается на экране с помощью функции show() из библиотеки Matplotlib.

Функция plot_seaborn использует библиотеку Seaborn для построения точечного графика на основе тех же данных, что и функция plot_matplotlib.


Функция plot_altair использует библиотеку Altair для построения круговой диаграммы на основе данных, которые хранятся в переменной data. График отображается в интерактивном формате с помощью библиотеки altair_viewer.

Функция plot_plotly использует библиотеку Plotly для построения трехмерного графика. Она получает данные из файла CSV, строит поверхность и отображает ее на экране с помощью функции plot() из библиотеки plotly.

Функция plot_bokeh использует библиотеку Bokeh для построения гексагонального графика на основе данных, которые хранятся в переменной data. Она получает случайные числа с помощью стандартного нормального распределения, затем строит гексагональную сетку на основе этих данных и отображает ее на экране с помощью функции figure() из библиотеки Bokeh.


Пример построения графика с помощью библиотеки PLOTLY представлен на рисунке ниже.
![image](https://github.com/daktanaev/graduate-work/assets/105858525/348df2e8-1b9c-41bd-9e36-75577a82eb57)
