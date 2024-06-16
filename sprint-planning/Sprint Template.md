---
tags: 
sprint start: 
sprint end:
---
## Sprint To Do

### Service Name

- [ ]

## Daily To Do at Glance

```dataviewjs
const startOfSprint = moment(dv.page('')["sprint start"]?.ts);
const endOfSprint = moment(dv.page('')["sprint end"]?.ts);

let day = startOfSprint;

while (day <= endOfSprint) {
	const formattedDay = moment(day.toDate()).format('[Planning]/YYYY/[Day]/MMMM/wo/YYYY-MM-DD(ddd)');

	dv.paragraph(dv.sectionLink(formattedDay, "Today To Do", true, formattedDay))

	day = day.clone().add(1, 'd');
};
```

## Daily Issues at a Glance

```dataviewjs
const startOfSprint = moment(dv.page('')["sprint start"]?.ts);
const endOfSprint = moment(dv.page('')["sprint end"]?.ts);

let day = startOfSprint;

while (day <= endOfSprint) {
	const formattedDay = moment(day.toDate()).format('[Planning]/YYYY/[Day]/MMMM/wo/YYYY-MM-DD(ddd)');

	dv.paragraph(dv.sectionLink(formattedDay, "Issues", true, formattedDay))

	day = day.clone().add(1, 'd');
};
```

## Sprint Postmortem

-
