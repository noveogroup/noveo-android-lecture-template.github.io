# Main Thread

По умолчанию все компоненты приложения работают в нём.
К View можно обращаться только из него.

Если занять более чем на 5 секунд, система покажет ANR (диалог Application Not Responding).

<div class="fragment" data-fragment-index="1">
Долгие операции в главном потоке - это плохо!
</div>

------

# Main Thread

<img src="https://noveogroup.github.io/university-android-presentations/lecture/network/img/queue.png" width="100%">