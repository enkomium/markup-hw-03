Как делается Сетка.

Задаем Флекс
задаем Перенос Врап!
задаем ширину отступов маржина каточкам и задаем отрицательные такие же значения Родителю карточек
Задаем Флкс Бэйсис в самой карточке и делим калькулятором 100% на 3 или скок надо
Делаем переменную для маржинов и заменяем
для отрицательного маржина умножаем переменную на -1 калькулятором

Потом оборачиваем текст в отдельный Див и задаем ему Паддинги!

Как добавлять картинки с помощью Псевдо-элементов!

- Элемент делаем Инлайн флексом
- по деланию центрируем все если надо сделать с боку.
- создаем псевдо-элемент где указываем КОНТЕНТ, РАЗМЕР ОБЛАСТИ для КАРТИНКИ, Отступ, повторение и т.д..
- Потом вставляем картинки с помощью других псевдо-элементов с дополнительными классами!

.contact-link {
display: inline-flex;
align-items: center;
color: var(--title-text-color);
/_ background-color: aqua; _/
text-decoration: none;
}

.contact-link::before {
content: "";
width: 20px;
height: 20px;
margin-right: 10px;
/_ background-color: red; _/
/_ background-image: url("../images/global/antenna\ 1.svg"); _/
background-repeat: no-repeat;
background-size: contain;
background-position: center;
}

.contact-link.mail::before {
background-image: url("../images/global/envelope\ \(hover\).svg");
}

.contact-link.tel::before {
background-image: url("../images/global/envelope\ \(hover\).svg");
}
