---
tags:
  -
---

## Weekly To Do
### Project Name
- [ ]

## Daily To Do at Glance

```dataviewjs
const createDay = `${dv.page('').file.cday}`
const startOfWeek = moment(createDay).startOf('week');
const endOfWeek = moment(createDay).endOf('week');

let day = startOfWeek;
while (day <= endOfWeek) {
	const formattedDay = moment(day.toDate()).format('YYYY-MM-DD(ddd)');

	dv.paragraph(dv.sectionLink(formattedDay, "Today To Do", true, formattedDay))

	day = day.clone().add(1, 'd');
};
```

## Weekly Postmortem
-

## Daily Postmortem at a Glance

```dataviewjs
const createDay = `${dv.page('').file.cday}`;
const startOfWeek = moment(createDay).startOf('week');
const endOfWeek = moment(createDay).endOf('week');

let day = startOfWeek;

while (day <= endOfWeek) {
	const formattedDay = moment(day.toDate()).format('YYYY-MM-DD(ddd)');

	dv.paragraph(dv.sectionLink(formattedDay, "Today Postmortem", true, formattedDay))

	day = day.clone().add(1, 'd');
};
```
