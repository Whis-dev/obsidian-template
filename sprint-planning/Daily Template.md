```dataviewjs
const todayDate = dv.page('').file.cday;
const sprintFolderPath = `Planning/${todayDate.year}/Sprint`
const sprintList = dv.pages(`"${sprintFolderPath}"`)
const findSprint = sprintList.values.find(sprint => sprint["sprint start"]?.ts <= todayDate.ts && todayDate.ts <= sprint["sprint end"]?.ts);

const sprintPath = findSprint?.file.path || `${sprintFolderPath}/${moment(todayDate.ts).format('MMMM')}/Sprint ${sprintList.length + 1}`



dv.paragraph(dv.sectionLink(sprintPath, "Sprint To Do", true, sprintPath))
```

### Today To Do

- [ ]

### Today Postmortem

-

### TIL

-

### Issues

-
