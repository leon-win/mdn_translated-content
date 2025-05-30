---
title: Введение
slug: Web/SVG/Tutorials/SVG_from_scratch/Introduction
---

{{SVGRef}}{{ PreviousNext("Web/SVG/Руководство", "Web/SVG/Руководство/Введение") }}

[SVG](/ru/docs/Web/SVG) это язык [XML](/en-US/XML) разметки, схожий с [XHTML](/en-US/XHTML), который может использоваться для рисования векторной графики, такой как та, что показана справа. Он может быть использован для создания изображения путём указания всех необходимых линий и форм, путём модификации уже существующих растровых изображений, или путём комбинации обоих. Изображения и их компоненты также могут быть трансформированы, собраны вместе, или отфильтрованы чтобы полностью изменить их внешний вид.

В 1999 году, после конкурса нескольких форматов, SVG был включён в [W3C](https://www.w3.org), однако полностью ратифицирован не был. SVG поддерживается всеми наиболее популярными [браузерами](https://caniuse.com/#search=svg). Недостатком использования SVG является его медленная загрузка . При этом SVG даёт некоторые преимущества, такие как наличие соответствующего [DOM interface](/ru/docs/Web/API), и отсутствие необходимости в стороннем расширении. Использовать данное решение или нет, часто зависит от конкретного случая применения.

### Базовые компоненты

В [HTML](/ru/docs/Web/HTML) имеются элементы для определения заголовков, параграфов, таблиц и т.п. В SVG, с другой стороны, имеются элементы для кругов, прямоугольников, и простых и сложных кривых. Простой SVG документ состоит из корневого элемента {{ SVGElement('svg') }} и нескольких основных форм, которые вместе обеспечивают построение рисунка. Кроме того, есть элемент {{ SVGElement('g') }}, который используется для группировки нескольких основных форм вместе.

Начиная с этого, SVG изображение может стать сколь угодно сложным. SVG поддерживает градиенты, вращения, фильтры, анимации, взаимодействие с JavaScript, и т.п. Но все эти дополнительные возможности языка полагаются на этот относительно небольшой набор элементов, определяющих графическую область.

### До начала работы

Существует ряд приложений для рисования, такие как [Inkscape](https://www.inkscape.org/), который свободный и использует SVG в качестве родного файлового формата. Однако, это руководство полагается только на надёжный XML или текстовый редактор (на ваш выбор). Идея в том, чтобы обучить основам SVG тех, кто хочет понять его, и это лучше всего сделать, самостоятельно поработав с разметкой. При этом вы должны знать свою конечную цель. Не все программы просмотра SVG одинаковы, и поэтому существует высокий шанс того, что написанное для одного приложения не будет отображаться таким же образом в другом, просто потому что они поддерживают разные уровни SVG детализации или другую детализацию, которую вы используете наряду с SVG (такую как, [JavaScript](/ru/docs/Web/JavaScript) или [CSS](/ru/docs/Web/CSS)).

SVG поддерживается всеми современными браузерами и даже, в некоторых случаях, паре их устаревших версий. Достаточно полную таблицу поддерживающих браузеров можно найти в [Can I use](http://caniuse.com/svg). Firefox поддерживает некоторый контент SVG, начиная с версии 1.5, и этот уровень поддержки растёт с каждым новым выпуском. К счастью, наряду с этим руководством, MDN может помочь разработчикам не отставать от изменений между Gecko и некоторыми другими основными реализациями.

Перед тем как начать, вы должны иметь основное понимание XML или другого языка разметки, такого как HTML. Если вы не очень знакомы с XML, ниже имеются некоторые рекомендации, которые следует иметь ввиду:

- Элементы и атрибуты SVG должны быть все введены в указанном регистре, поскольку XML обладает чувствительностью к регистру (в отличии от HTML).
- Значения атрибутов в SVG должны быть помещены внутри кавычек, даже если они являются цифрами.

SVG имеет довольно большую спецификацию. Это руководство охватывает только основы. После ознакомления с ними, тебе следует использовать [Справочник SVG элементов](/ru/docs/Web/SVG/%D0%AD%D0%BB%D0%B5%D0%BC%D0%B5%D0%BD%D1%82) и [SVG интерфейсы](/ru/docs/Web/API/Document_Object_Model#svg_интерфейсы), чтобы найти что-либо ещё при необходимости.

### Особенности SVG

Начиная с рекомендации 2003 года, самой свежей "полной" версией SVG является версия 1.1. Она построена на SVG 1.0, но содержит также больше модульности для упрощения реализации. [Второй выпуск SVG 1.1](https://www.w3.org/TR/SVG/) стал Рекомендацией в 2011 году. "Полная" версия SVG 1.2 стала следующим главным выпуском SVG. Ей пришла на смену развивающаяся [SVG 2.0](https://www.w3.org/TR/SVG2/), которая сейчас усиленно разрабатывается и следует схожему с CSS 3 подходу, в котором она разделяет компоненты в несколько свободно связанных специфирований.

Кроме полных рекомендаций SVG, рабочая группа при W3C ввела SVG Tiny и SVG Basic в 2003 году. Эти две версии нацелены главным образом на мобильные устройства. Первый, SVG Tiny, должен выдавать графические примитивы для небольших устройств с низкими возможностями. SVG Basic имеет много общего с полным SVG, но не включает те компоненты, что трудны для реализации или являются тяжёлыми для воспроизведения (как анимации). В 2008, SVG Tiny 1.2 стала Рекомендацией W3C.

Существовали планы для спецификации SVG Print, которая имела бы поддержку для множества страниц и улучшенное управление цветом. Эта работа была прекращена.

{{ PreviousNext("Web/SVG/Tutorial", "Web/SVG/Tutorial/Getting_Started") }}
