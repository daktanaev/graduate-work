import sys
import pandas as pd
from numpy.random import standard_normal
import matplotlib.pyplot as plt
import seaborn as sns
import altair as alt
import altair_viewer
import plotly.graph_objs as go
import plotly.offline as pyo
import plotly.express as px
from bokeh.models import ColumnDataSource, HoverTool
from bokeh.plotting import figure, output_file, show

from bokeh.transform import linear_cmap
from bokeh.util.hex import hexbin
from PyQt5.QtCore import Qt
from PyQt5.QtWidgets import QApplication, QMainWindow, QFileDialog, QMessageBox, QLabel, QLineEdit, QPushButton, \
    QVBoxLayout, QHBoxLayout, QComboBox, QGroupBox, QWidget
from PyQt5.QtGui import QPixmap
from PyQt5.QtGui import QImage


class MainWindow(QMainWindow):
    def __init__(self):
        super().__init__()

        self.setWindowTitle("Визуализация данных из Excel")
        self.setGeometry(200, 200, 1000, 600)

        # Создание основного виджета
        widget = QWidget()
        self.setCentralWidget(widget)

        # Создание макетов
        main_layout = QVBoxLayout()
        widget.setLayout(main_layout)

        # Создание макетов для загрузки файла и выбора листа
        file_layout = QHBoxLayout()
        sheet_layout = QHBoxLayout()
        main_layout.addLayout(file_layout)
        main_layout.addLayout(sheet_layout)

        # Создание метки и поля ввода для пути к файлу
        file_label = QLabel("Выберите файл:")
        file_layout.addWidget(file_label)

        self.file_line = QLineEdit()
        self.file_line.setReadOnly(True)
        file_layout.addWidget(self.file_line)

        file_button = QPushButton("Обзор")
        file_button.clicked.connect(self.browse_file)
        file_layout.addWidget(file_button)

        # Создание метки и выпадающего списка для выбора листа
        sheet_label = QLabel("Выберите лист:")
        sheet_layout.addWidget(sheet_label)

        self.sheet_combo = QComboBox()
        self.sheet_combo.activated[str].connect(self.select_sheet)
        sheet_layout.addWidget(self.sheet_combo)

        # Создание кнопок для визуализации данных
        plot_layout = QHBoxLayout()
        main_layout.addLayout(plot_layout)

        plot_matplotlib_button = QPushButton("График")
        plot_matplotlib_button.clicked.connect(self.plot_matplotlib)
        #plot_layout.addWidget(plot_matplotlib_button)


        #('C:\\Users\\Epistaxis\\Pictures\\GameCenter\\LostArk\\1.jpg'))

        # Создание группы для кнопки Matplotlib и изображения
        group_matplotlib = QGroupBox("График с помощью Matplotlib")
        group_matplotlib_layout = QVBoxLayout()
        group_matplotlib.setLayout(group_matplotlib_layout)
        group_matplotlib.setMaximumSize(400, 200)

        # Добавление кнопки в группу
        group_matplotlib_layout.addWidget(plot_matplotlib_button)

        # Загрузка изображения и добавление его в группу
        icon_matplotlib = QPixmap.fromImage(QImage('C:\\Users\\Epistaxis\\Desktop\\Диплом\\Проект\\math.png'))
        label_matplotlib = QLabel()
        label_matplotlib.setPixmap(icon_matplotlib.scaled(200, 200, Qt.KeepAspectRatio, Qt.SmoothTransformation))
        label_matplotlib.setMinimumSize(100, 100)
        label_matplotlib.setAlignment(Qt.AlignCenter)
        group_matplotlib_layout.addWidget(label_matplotlib)

        # Добавление группы в главный макет
        plot_layout.addWidget(group_matplotlib)

        ##############
        plot_seaborn_button = QPushButton("Диаграмма рассеяния")
        plot_seaborn_button.clicked.connect(self.plot_seaborn)
      #  plot_layout.addWidget(plot_seaborn_button)

        # Создание группы для кнопки Matplotlib и изображения
        group_seaborn = QGroupBox("График с помощью Seaborn")
        group_seaborn_layout = QVBoxLayout()
        group_seaborn.setLayout(group_seaborn_layout)
        group_seaborn.setMaximumSize(400, 200)

        # Добавление кнопки в группу
        group_seaborn_layout.addWidget(plot_seaborn_button)

        # Загрузка изображения и добавление его в группу
        icon_seaborn = QPixmap.fromImage(QImage('C:\\Users\\Epistaxis\\Desktop\\Диплом\\Проект\\seaborn.png'))
        label_seaborn = QLabel()
        label_seaborn.setPixmap(icon_seaborn.scaled(200, 200, Qt.KeepAspectRatio, Qt.SmoothTransformation))
        label_seaborn.setMinimumSize(100, 100)
        label_seaborn.setAlignment(Qt.AlignCenter)
        group_seaborn_layout.addWidget(label_seaborn)

        # Добавление группы в главный макет
        plot_layout.addWidget(group_seaborn)
##################
        # plot_altair_button = QPushButton("Altair")
        # plot_altair_button.clicked.connect(self.plot_altair)
        # plot_layout.addWidget(plot_altair_button)
        #
        # # Создание вертикального макета для изображения и кнопки
        # altair_image_layout = QVBoxLayout()
        #
        # # Загрузка изображения для Altair
        # icon_altair = QPixmap.fromImage(
        #     QImage(
        #         'C:\\Users\\Epistaxis\\Pictures\\GameCenter\\AtomicHeart\\1.jpg'))  # замените 'path_to_image' на путь к вашему изображению
        # label_altair = QLabel()
        # label_altair.setPixmap(icon_altair.scaled(100, 100, Qt.KeepAspectRatio, Qt.SmoothTransformation))
        #
        # # Добавление изображения в вертикальный макет
        # altair_image_layout.addWidget(label_altair)
        #
        # # Добавление кнопки в вертикальный макет
        # altair_image_layout.addWidget(plot_altair_button)
        #
        # # Добавление вертикального макета в главный вертикальный макет
        # plot_layout.addLayout(altair_image_layout)
######
        plot_plotly_button = QPushButton("3D график")
        plot_plotly_button.clicked.connect(self.plot_plotly)
      #  plot_layout.addWidget(plot_plotly_button)

        # Создание группы для кнопки plotly и изображения
        group_plotly = QGroupBox("График с помощью Plotly")
        group_plotly_layout = QVBoxLayout()
        group_plotly.setLayout(group_plotly_layout)
        group_plotly.setMaximumSize(400, 200)

        # Добавление кнопки в группу
        group_plotly_layout.addWidget(plot_plotly_button)

        # Загрузка изображения и добавление его в группу
        icon_plotly = QPixmap.fromImage(QImage('C:\\Users\\Epistaxis\\Desktop\\Диплом\\Проект\\plotly.png'))
        label_plotly = QLabel()
        label_plotly.setPixmap(icon_plotly.scaled(200, 200, Qt.KeepAspectRatio, Qt.SmoothTransformation))
        label_plotly.setMinimumSize(100, 100)
        label_plotly.setAlignment(Qt.AlignCenter)
        group_plotly_layout.addWidget(label_plotly)

        # Добавление группы в главный макет
        plot_layout.addWidget(group_plotly)
##########
        plot_bokeh_button = QPushButton("Цветовая карта")
        plot_bokeh_button.clicked.connect(self.plot_bokeh)
        plot_layout.addWidget(plot_bokeh_button)

        # Создание группы для кнопки bokeh и изображения
        group_bokeh = QGroupBox("График с помощью Bokeh")
        group_bokeh_layout = QVBoxLayout()
        group_bokeh.setLayout(group_bokeh_layout)
        group_bokeh.setMaximumSize(400, 200)

        # Добавление кнопки в группу
        group_bokeh_layout.addWidget(plot_bokeh_button)

        # Загрузка изображения и добавление его в группу
        icon_bokeh = QPixmap.fromImage(QImage('C:\\Users\\Epistaxis\\Desktop\\Диплом\\Проект\\bokeh.png'))
        label_bokeh = QLabel()
        label_bokeh.setPixmap(icon_bokeh.scaled(200, 200, Qt.KeepAspectRatio, Qt.SmoothTransformation))
        label_bokeh.setMinimumSize(100, 100)
        label_bokeh.setAlignment(Qt.AlignCenter)
        group_bokeh_layout.addWidget(label_bokeh)

        # Добавление группы в главный макет
        plot_layout.addWidget(group_bokeh)
########
        # Инициализация переменных для хранения данных
        self.file_path = None
        self.sheet_names = None
        self.selected_sheet = None
        self.data = None

        self.show()

# Функция для загрузки файла Excel
    def browse_file(self):
        options = QFileDialog.Options()
        options |= QFileDialog.DontUseNativeDialog
        file_path, _ = QFileDialog.getOpenFileName(self, "Выберите файл Excel", "", "Excel Files (*.xlsx *.xls)")
        if file_path:
            self.file_path = file_path
            self.file_line.setText(file_path)
            print('Файл загружен')

            # Получение имен листов
            self.sheet_names = pd.ExcelFile(self.file_path).sheet_names
            self.sheet_combo.addItems(self.sheet_names)

    # Функция для выбора листа
    def select_sheet(self, text):
        self.selected_sheet = text

        # Чтение данных из листа
        if self.file_path is not None:
            #self.data = pd.read_excel(xlsx, 'Sheet1')
            self.data = pd.read_excel(self.file_path, sheet_name=self.selected_sheet)

            print('Лист выбран ')
            #self.data = pd.read_excel('C:\\Users\\ITAdmin\\Downloads\\1.xlsx', sheet_name=self.selected_sheet)

    # Функция для визуализации данных с помощью библиотеки Matplotlib
    def plot_matplotlib(self):
        if self.data is not None:
            # Построение графика
            fig, ax = plt.subplots()
            x = [10, 4, 6, 1]
            y = [1, 2, 3, 4]
           # ax.plot(x, y)
            ax.plot(self.data['x'], self.data['y'])
            #ax.plot(self.data['x'], self.data['y1'])
            #ax.plot(self.data[1], y)
            ax.set_xlabel('x')
            ax.set_ylabel('y')
            ax.set_title('График с помощью Matplotlib')
            plt.show()

    # Функция для визуализации данных с помощью библиотеки Seaborn
    def plot_seaborn(self):
        if self.data is not None:
            # Построение графика
            tips = self.data
            sns.set(color_codes=True)
            ax = sns.scatterplot(
                x="x",
                y="y",
                data=tips
            )
            #sns.lineplot(x='x', y='y', data=self.data)
            plt.xlabel('x')
            plt.ylabel('y')
            plt.title('График с помощью Seaborn')
            plt.show()

    # Функция для визуализации данных с помощью библиотеки Altair
    def plot_altair(self):
        if self.data is not None:
            chart = alt.Chart(self.data).mark_line().encode(
                x='x',
                y='y'
            ).interactive()
            altair_viewer.show(chart)

    # Функция для визуализации данных с помощью библиотеки Plotly
    def plot_plotly(self):
        if self.data is not None:
            # Построение графика
            z_data = pd.read_csv(
                'C:\\Users\\Epistaxis\\Desktop\\Диплом\\Проект\\count.csv')

            fig = go.Figure(data=[go.Surface(z=z_data.values)])
            fig.update_traces(contours_z=dict(show=True, usecolormap=True,
                                              highlightcolor="limegreen", project_z=True))
            fig.update_layout(title='Mt Bruno Elevation', autosize=False,
                              scene_camera_eye=dict(x=1.87, y=0.88, z=-0.64),
                              width=1920, height=1080,
                              margin=dict(l=65, r=50, b=65, t=90)
                              )

            pyo.plot(fig, filename='plotly.html', auto_open=True)

            # fig = go.Figure(data=[go.Scatter(x=self.data['x'], y=self.data['y'])])
            # fig.update_layout(title='График с помощью Plotly', xaxis_title='x', yaxis_title='y')
            # pyo.plot(fig, filename='plot.html', auto_open=True)

    # Функция для визуализации данных с помощью библиотеки Bokeh
    def plot_bokeh(self):
        if self.data is not None:
            # Построение графика

            x = standard_normal(50000)
            y = standard_normal(50000)
            #x = self.data['x']
            #y = self.data['y']
            for item in x:
                print(item)

            bins = hexbin(x, y, 0.1)

            p = figure(tools="", match_aspect=True, background_fill_color='#440154')
            p.grid.visible = False

            p.hex_tile(q="q", r="r", size=0.1, line_color=None, source=bins,
                       fill_color=linear_cmap('counts', 'Viridis256', 0, max(bins.counts)))

            show(p)
            # output_file("bokeh_plot.html")
            # p = figure(title="График с помощью Bokeh", x_axis_label='x', y_axis_label='y')
            # p.line(self.data['x'], self.data['y'], legend_label="y=x^2", line_width=2)
            # show(p)
            # # Построение интерактивного графика
            # source = ColumnDataSource(self.data)
            # hover = HoverTool(tooltips=[('x', '@x'), ('y', '@y')])
            # p = figure(title="Интерактивный график с помощью Bokeh", x_axis_label='x', y_axis_label='y', tools=[hover])
            # p.line('x', 'y', source=source, legend_label="y=x^2", line_width=2)
            # show(p)


if __name__ == '__main__':
    app = QApplication(sys.argv)
    window = MainWindow()
    window.show()
    sys.exit(app.exec_())
