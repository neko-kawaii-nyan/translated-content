---
title: '<dd>: Элемент описания определения'
slug: Web/HTML/Element/dd
tags:
  - Description Details
  - Element
  - HTML
  - Reference
  - Web
  - dd
  - Веб
  - Список определений
  - Элемент
  - списки
translation_of: Web/HTML/Element/dd
---

{{HTMLSidebar}}

**HTML-элемент `<dd>`** (_от англ. Description Details_) предоставляет подробности или определение предшествующего термина ({{HTMLElement("dt")}}) в списке определений ({{HTMLElement("dl")}}).

{{EmbedInteractiveExample("pages/tabbed/dd.html", "tabbed-standard")}}

| [Категории контента](/ru/docs/Web/Guide/HTML/Content_categories) | Нет                                                                                                                                                                                                                                          |
| ---------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Допустимое содержимое                                            | [Потоковый контент](/ru/docs/Web/Guide/HTML/Content_categories#Потоковый_контент)                                                                                                                                                            |
| Пропуск тегов                                                    | Открывающий тег обязателен. Конечный тег может быть опущен, если за элементом {{HTMLElement("dd")}} непосредственно следует элемент `<dd>` или {{HTMLElement("dt")}}, или если в родительском элементе нет больше содержимого.               |
| Допустимые родители                                              | Элементы {{HTMLElement("dl")}} и {{HTMLElement("div")}}, находящийся внутри элемента {{HTMLElement("dl")}}. Может быть использован после {{HTMLElement("dt")}} или другого элемента {{HTMLElement("dd")}}.                                   |
| Неявные ARIA-роли                                                | [`definition`](/ru/docs/Web/Accessibility/ARIA/Roles/definition_role)                                                                                                                                                                    |
| Допустимые ARIA-роли                                             | Нет                                                                                                                                                                                                                                          |
| DOM-интерфейс                                                    | {{domxref("HTMLElement")}}                                                                                                                                                                                                                   |

## Атрибуты

Этот элемент включает [глобальные атрибуты](/ru/docs/Web/HTML/Общие_атрибуты).

- {{htmlattrdef("nowrap")}} {{Non-standard_inline}}
  - : Если значение атрибута установлено `yes`, текст определения не будет переноситься. Значение по умолчанию `no`.

## Пример

Для примера смотрите [образец для \<dl> элемента](/ru/docs/HTML/Element/dl#examples).

## Спецификации

{{Specifications}}

## Поддержка браузерами

{{Compat}}

## Смотрите также

- {{HTMLELement("dl")}}
- {{HTMLElement("dt")}}
