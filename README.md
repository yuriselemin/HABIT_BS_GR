
<h1 align="center">HABIT</h1>


Это приложение представляет собой систему для отслеживания привычек, включающую регистрацию пользователей, добавление привычек, ежедневную фиксацию прогресса и ограничение процесса выработки привычки минимальным сроком в 40 дней.
Давайте рассмотрим, как оно работает шаг за шагом.
<p>
<h2>1. Структура проекта</h2>
  <p>  
Проект состоит из следующих основных компонентов:
Модели: Определяют структуру данных, таких как информация о пользователе, привычках и ежедневном прогрессе.
Представления: Управляют логикой взаимодействия с пользователями, включая регистрацию, добавление привычек и фиксацию прогресса.
Формы: Используются для ввода данных пользователем, например, для регистрации и добавления привычек.
Шаблоны: Содержат HTML-код для визуального представления данных пользователям.
URL'ы: Определяют маршруты для различных страниц приложения.
  </p>
</p>
<p>
<h2>2. Процесс работы приложения</h2>
    <p> 
Регистрация пользователя
      
Когда пользователь впервые посещает сайт, он попадает на страницу welcome, где ему предлагается зарегистрироваться. Форма регистрации использует класс RegistrationForm, основанный на ModelForm, что позволяет легко создавать новых пользователей. После успешной регистрации пользователь автоматически входит в систему и перенаправляется на домашнюю страницу.
    <p> 
</p>
Домашняя страница:

На домашней странице (home) отображаются все привычки текущего пользователя. Если привычек нет, пользователю предлагается создать первую привычку. Для каждого элемента списка привычек доступна ссылка для фиксации ежедневного прогресса.

Добавление привычки:

При нажатии на кнопку "Добавить новую привычку" пользователь попадает на страницу add_habit, где он может ввести название новой привычки. Дата начала и окончания устанавливаются автоматически (окончание через 40 дней).

Ежедневная фиксация прогресса:

Для каждой привычки пользователь может ежедневно отмечать выполнение задачи. Для этого он переходит по соответствующей ссылке на страницу daily_progress, где отмечает, выполнена ли задача за текущий день.

Основные компоненты и их взаимодействие:

Модель Habit: Хранит информацию о привычке, такую как название, даты начала и конца.

Модель DailyProgress: Связана с моделью Habit, хранит информацию об успешности выполнения привычки в конкретный день.

Форма RegistrationForm: Используется для регистрации новых пользователей.

Маршруты:
Определены в файле urls.py и связывают URL-адреса с соответствующими представлениями.
Базовый шаблон base.html: Содержит общую разметку для всех страниц, включая хедер и футер.

Заключение:
Приложение помогает пользователям регистрироваться, добавлять привычки и отслеживать их выполнение на протяжении определенного времени. Оно имеет простую и интуитивно понятную структуру, облегчая управление своими привычками.

