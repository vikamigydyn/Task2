## Лабораторная работа №2. Основы верстки
## Выполнила: Мигыдын Вика, ИСП-211о

# 1. Обзор
Приложение состоит из четырех активностей, каждая из которых содержит кнопки для навигации.

# 2. Структура
- "MainActivity": Основная активность с кнопками для перехода ко всем остальным активностям.
- "MainActivity2": Вторая активность с набором кнопок.
- "MainActivity3": Третья активность с кнопками, расположенными по центру и по краям.
- "MainActivity4": Четвертая активность с кастомизированной кнопкой.

# 3. MainActivity
На данном экране расположены кнопки:
Кнопка 1 "Перейти к экрану 2": При нажатии запускает MainActivity2.
Кнопка 2 "Перейти к экрану 3": При нажатии запускает MainActivity3.
Кнопка 3 "Перейти к экрану 4": При нажатии запускает MainActivity4.
Кнопка 4 "Выйти": При нажатии завершает текущую активность (выход из приложения).
![скрин1.png](..%2F..%2F..%2F..%2F%F1%EA%F0%E8%ED1.png)

# 3. MainActivity2
Второй экран создан с использованием LinearLayout. Он состоит из 7 кнопок:

- 3 расположены в верхней части экрана android:layout_gravity="top"
- 2 расположены по центру android:layout_gravity="center"
- 3 расположены в нижней части экрана android:layout_gravity="bottom"
![скрин2.png](..%2F..%2F..%2F..%2F%F1%EA%F0%E8%ED2.png)

# 4. MainActivity3
Третий экран создан с использованием RelativeLayout. Он состоит из 6 кнопок:

- 2 расположены в верхней части экрана и занимают по половине экрана android:layout_toLeftOf = "@+id/view"
android:layout_toRightOf="@+id/view"
- 3 расположены по центру android:layout_centerInParent="true" android:layout_toLeftOf="@+id/button15" android:layout_toRightOf="@+id/button15"
- 1 расположена в нижней части экрана
![скрин3.png](..%2F..%2F..%2F..%2F%F1%EA%F0%E8%ED3.png)

# 5. MainActivity4
На четвертом экране расположена одна кнопка, которая при нажатии меняет свой цвет. Толщина обводки 3px, так как месяц моего рождения - март. Чтобы кнопка приобрела эти функции, был создан файл "my_button".
`<item android:state_focused="false"
android:state_pressed="false"
android:state_enabled="true">
<shape xmlns:android="http://schemas.android.com/apk/res/android"
android:shape="rectangle" >
<solid android:color="#27572c" />
<corners android:radius="24dp"/>
<stroke android:width="3px" android:color="#505050" />
</shape>
</item>
    <item android:state_focused="false"
        android:state_pressed="true"
        android:state_enabled="true">
        <shape xmlns:android="http://schemas.android.com/apk/res/android"
            android:shape="rectangle" >
            <solid android:color="@android:color/holo_green_light" />
            <corners android:radius="24dp"/>
            <stroke android:width="3px" android:color="#505050" />
        </shape>
    </item>`
![скрин5.png](..%2F..%2F..%2F..%2F%F1%EA%F0%E8%ED5.png)
![скрин6.png](..%2F..%2F..%2F..%2F%F1%EA%F0%E8%ED6.png)
