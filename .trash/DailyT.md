---
<%* 
let url = 'https://www.tianqi.com/jinan/'
let res = await request({url: url,method: "GET"});
res = res.replace(/\s/g,'') 
r=/<ddclass="weather">[\s\S]*?<\/dd>/g
let data = r.exec(res)[0] 
r = /<span><b>(.*?)<\/b>(.*?)<\/span>/g---
type: OKR
tags:
  - review/daily
date: 2024-07-23-星期二
weather: 济南 小雨 20~26℃
Habit_1:
Habit_2:
Habit_3:
Habit_4:
---

<div style="font-size: 28px;color:#A27E7E"> 🍳 </div>

## LIST OF PROGRESS


<div class="life-container" style="width:100%;">
	<div class="life-progress progress-day">0%</div>
</div>

<div class="life-container" style="width:100%;">
	<div class="life-progress progress-month">0%</div>
</div>

<div class="life-container" style="width:100%;">
	<div class="life-progress progress-year">0%</div>
</div>

```dataviewjs
setInterval(refreshBar,1000) // 刷新间隔为1秒

const monthsLeap = [31,29,31,30,31,30,31,31,30,31,30,31]
const monthsCommon = [31,28,31,30,31,30,31,31,30,31,30,31]

const greenBG = 'repeating-linear-gradient(45deg, #13ce66 0, #13ce66 10px, #36d57d 10px, #36d57d 20px)'; // 进度条在 0~25% 之间的背景, 背景为绿色
const blueBG = 'repeating-linear-gradient(45deg, #50bfff 0, #50bfff 10px, #6ac9ff 10px, #6ac9ff 20px)'; // 进度条在 25~50% 之间的背景, 背景为蓝色
const yellowBG = 'repeating-linear-gradient(45deg, #f7ba2a 0, #f7ba2a 10px, #f8c44a 10px, #f8c44a 20px)'; // 进度条在 50~75% 之间的背景, 背景为黄色
const redBG = 'repeating-linear-gradient(45deg, #ff4949 0, #ff4949 10px, #ff6464 10px, #ff6464 20px)'; // 进度条在 75%~100% 之间的背景, 背景为红色

function refreshBar(){
	let date = new Date()
	let passMinutes = date.getHours()*60+date.getMinutes()
    let passDate = date.getDate()
	let month = date.getMonth()
	let year = date.getFullYear()

	let barsDay = document.getElementsByClassName("progress-day")
    let barsMonth =document.getElementsByClassName("progress-month")
    let barsYear = document.getElementsByClassName("progress-year")
    
	for(let i = 0; i < barsDay.length; i++){
		let per = passMinutes / (24*60)
		if(per < 0.25){
			barsDay[i].style.backgroundImage = greenBG;
		} else if(per < 0.5){
			barsDay[i].style.backgroundImage = blueBG;
		} else if(per < 0.75){
			barsDay[i].style.backgroundImage = yellowBG;
		} else {
			barsDay[i].style.backgroundImage = redBG;
		}
		barsDay[i].style.color = "#f1c2e8";
		barsDay[i].style.fontWeight = "bold";
		barsDay[i].style.width = per * 100 + "%"
		barsDay[i].innerHTML = "D: " + (per * 100).toFixed(0) + "%";		
	}

    for(let i = 0; i < barsMonth.length; i++){
		let per;
		if(year % 4 == 0 && year % 100 != 0 || year % 400 == 0){
			per = passDate / monthsLeap[month]
		} else {
			per = passDate / monthsCommon[month]
		}
		if(per < 0.25){
			barsMonth[i].style.backgroundImage = greenBG;
		} else if(per < 0.5){
			barsMonth[i].style.backgroundImage = blueBG;
		} else if(per < 0.75){
			barsMonth[i].style.backgroundImage = yellowBG;
		} else {
			barsMonth[i].style.backgroundImage = redBG;
		}
		barsMonth[i].style.color = "#f1c2e8";
		barsMonth[i].style.fontWeight = "bold";
		barsMonth[i].style.width = per * 100 + "%"
		barsMonth[i].innerHTML = "M:" + (per * 100).toFixed(0) + "%";
	}
	for(let i = 0; i < barsYear.length; i++){
		let per;
		let passDays = date.getDate();
		if(year % 4 == 0 && year % 100 != 0 || year % 400 == 0){
		for(let i = 0; i < month; i++){
			passDays += monthsLeap[i]
		}
			per = passDays / 366
		} else {
		for(let i = 0; i < month; i++){
			passDays += monthsCommon[i]
		}
			per = passDays / 365
		}
		if(per < 0.25){
			barsYear[i].style.backgroundImage = greenBG;
		} else if(per < 0.5){
			barsYear[i].style.backgroundImage = blueBG;
		} else if(per < 0.75){
			barsYear[i].style.backgroundImage = yellowBG;
		} else {
			barsYear[i].style.backgroundImage = redBG;
		}
		barsYear[i].style.fontWeight = "bold";
		barsYear[i].style.width = per * 100 + "%"
		barsYear[i].innerHTML = "Y: " + (per * 100).toFixed(0) + "%";
	}
}
```

## DIRECTION

> [!caution] 注意
> 根据自己笔记库中对于weekly review的命名规则，修改下面这个语句，让它可以自动嵌入上周的weekly review中关于本周计划的部分。

![[Weekly 2024-35#This week]]

## GET READY

###  Morning Checklist

- [ ] 整理起居
- [ ] 充足饮水
- [ ] 晨练晨跑
- [ ] 深度思考10min
- [ ] 整理工作桌面

### Confirmations
- 

### GTD & Top 3 Tasks

> [!NOTE]+ Get Things Done
> **1. 收集**：收集所有任务、想法、计划、待办事项。
> **2. 组织**：审视待办任务，分类所有任务和行动步骤，并回顾过往未完成的项目。
> > **2.1 分类**：根据任务属性（环境Context、项目Project、状态Status、截止时间Due）分类，单独任务、父子任务、项目类属任务...
> > 
> > **2.2 回顾**：定期回顾+跟踪进度，优先级排序。
> 
> **3. 执行**：专注于当前任务，避免分散注意力，提高工作效率。

### Todo list

-[ ]
-[ ]
-[ ]
-[ ]
-[ ]



## RELATIONSHIP

> [!caution] 注意
> 根据个人需求，修改dataview中的时间，让跟进的时间间隔符合你自己的要求

### Family
 ```dataview
table without ID
file.link as "Family", date_last_spoken as "Last Time"
from #people/family 
where follow_up = true
and date_last_spoken <= date(today) - dur(2 days)
```

### Friend
```dataview
table without ID
file.link as Friend, date_last_spoken as "Last Time"
from #people/friend
where follow_up = true
and date_last_spoken <= date(today) - dur(1 week)
```
 `dice: #people/friend|link`
 
### Client
```dataview
table without id file.link as Client, date_last_spoken as "Last Time"
from #people/client 
where follow_up = true
and date_last_spoken <= date(today) - dur(2 week)
```
 `dice: #people/client|link`
 
## REVIEW
### Go Back To The Future

> [!caution] 注意
> 把标签换成你日记的标签就可以了

 `dice: #review/daily|link`
### What happened today?
#### Project

> [!important] Prompt
> 今天关于项目的内容，请按照以下步骤进行复盘: 
> 1.回顾目标 2.叙述过程（5W1H）3.评估结果（SWOT）4.分析原因 （5WHYs） 5.推演规律  6.记录归档 

*Achivement*

*Opportunity*

*Action Plan*


#### About Today

 *win*

*struggle*

*other*


#### Idea


### Be Grateful!
- 

## END-OF-DAY CHECKLIST
- [ ] GTD
- [ ] bookkeeping
- [ ] review bookmarks
- [ ] check [[Habit Tracker]]
- [ ] Back Up
	- [ ] Time Machine
	- [ ] Obsidian Vault
- [ ] clean up the photos and videos
- [ ] check e-mail inbox

## NOTES

> [!caution] 注意
> 这边dataview报错不用担心，因为我在中间写了一句templater的语句，套用模板的时候会自动变成当天日期，这个dataview语句就可以正常运作了
### Notes created today
```dataview
list
where file.cday = date(2024-07-23)
sort file.ctime asc
```
### Notes modified today
```dataview
list
where file.mday = date(2024-07-23)
sort file.mtime asc
```

## HABIT TRACKER

> [!caution] 注意
> dataviewjs中需要修改的位置，已经在代码备注中用中文注明了

```dataviewjs
dv.span("**Habit_1**")  // 这里需要修改
const calendarData = {
    year: 2024,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages('"daily"').where(p => p.Habit_1)) {
    //dv.span("<br>" + page.file.name) 这里需要修改// uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        intensity: page.Habit_1, // (required) the data you want to track, will map color intensities automatically 这里需要修改
        content: "",           // (optional) Add text to the date cell
        color: "orange",          // (optional) Reference from 这里改成自己需要的颜色*calendarData.colors*. If no color is supplied; colors[0] is used
    })
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Habit_2**") 
const calendarData = {
    year: 2024,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages('"daily"').where(p => p.Habit_2)) {
    //dv.span("<br>" + page.file.name) // uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        intensity: page.Habit_2, // (required) the data you want to track, will map color intensities automatically
        content: "",           // (optional) Add text to the date cell
        color: "pink",          // (optional) Reference from *calendarData.colors*. If no color is supplied; colors[0] is used
    })
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Habit_3**") 
const calendarData = {
    year: 2024,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages('"daily"').where(p => p.Habit_3)) {
    //dv.span("<br>" + page.file.name) // uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        intensity: page.Habit_3, // (required) the data you want to track, will map color intensities automatically
        content: "",           // (optional) Add text to the date cell
        color: "blue",          // (optional) Reference from *calendarData.colors*. If no color is supplied; colors[0] is used
    })
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Habit_4**") 
const calendarData = {
    year: 2024,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages('"daily"').where(p => p.Habit_4)) {
    //dv.span("<br>" + page.file.name) // uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        intensity: page.Habit_4, // (required) the data you want to track, will map color intensities automatically
        content: "",           // (optional) Add text to the date cell
        color: "green",          // (optional) Reference from *calendarData.colors*. If no color is supplied; colors[0] is used
    })
}

renderHeatmapCalendar(this.container, calendarData)
```

data = r.exec(data)
let weather = '济南'+' '+data[1]+' '+data[2]
-%>
type: OKR
tags:
  - review/daily
date: <% tp.file.creation_date("YYYY-MM-DD-dddd") %>
weather: <% weather %>
Habit_1:
Habit_2:
Habit_3:
Habit_4:
---

<div style="font-size: 28px;color:#A27E7E"> 🍳 </div>


## LIST OF PROGRESS


<div class="life-container" style="width:100%;">
	<div class="life-progress progress-day">0%</div>
</div>

<div class="life-container" style="width:100%;">
	<div class="life-progress progress-month">0%</div>
</div>

<div class="life-container" style="width:100%;">
	<div class="life-progress progress-year">0%</div>
</div>

```dataviewjs
setInterval(refreshBar,1000) // 刷新间隔为1秒

const monthsLeap = [31,29,31,30,31,30,31,31,30,31,30,31]
const monthsCommon = [31,28,31,30,31,30,31,31,30,31,30,31]

const greenBG = 'repeating-linear-gradient(45deg, #13ce66 0, #13ce66 10px, #36d57d 10px, #36d57d 20px)'; // 进度条在 0~25% 之间的背景, 背景为绿色
const blueBG = 'repeating-linear-gradient(45deg, #50bfff 0, #50bfff 10px, #6ac9ff 10px, #6ac9ff 20px)'; // 进度条在 25~50% 之间的背景, 背景为蓝色
const yellowBG = 'repeating-linear-gradient(45deg, #f7ba2a 0, #f7ba2a 10px, #f8c44a 10px, #f8c44a 20px)'; // 进度条在 50~75% 之间的背景, 背景为黄色
const redBG = 'repeating-linear-gradient(45deg, #ff4949 0, #ff4949 10px, #ff6464 10px, #ff6464 20px)'; // 进度条在 75%~100% 之间的背景, 背景为红色

function refreshBar(){
	let date = new Date()
	let passMinutes = date.getHours()*60+date.getMinutes()
    let passDate = date.getDate()
	let month = date.getMonth()
	let year = date.getFullYear()

	let barsDay = document.getElementsByClassName("progress-day")
    let barsMonth =document.getElementsByClassName("progress-month")
    let barsYear = document.getElementsByClassName("progress-year")
    
	for(let i = 0; i < barsDay.length; i++){
		let per = passMinutes / (24*60)
		if(per < 0.25){
			barsDay[i].style.backgroundImage = greenBG;
		} else if(per < 0.5){
			barsDay[i].style.backgroundImage = blueBG;
		} else if(per < 0.75){
			barsDay[i].style.backgroundImage = yellowBG;
		} else {
			barsDay[i].style.backgroundImage = redBG;
		}
		barsDay[i].style.color = "#f1c2e8";
		barsDay[i].style.fontWeight = "bold";
		barsDay[i].style.width = per * 100 + "%"
		barsDay[i].innerHTML = "D: " + (per * 100).toFixed(0) + "%";		
	}

    for(let i = 0; i < barsMonth.length; i++){
		let per;
		if(year % 4 == 0 && year % 100 != 0 || year % 400 == 0){
			per = passDate / monthsLeap[month]
		} else {
			per = passDate / monthsCommon[month]
		}
		if(per < 0.25){
			barsMonth[i].style.backgroundImage = greenBG;
		} else if(per < 0.5){
			barsMonth[i].style.backgroundImage = blueBG;
		} else if(per < 0.75){
			barsMonth[i].style.backgroundImage = yellowBG;
		} else {
			barsMonth[i].style.backgroundImage = redBG;
		}
		barsMonth[i].style.color = "#f1c2e8";
		barsMonth[i].style.fontWeight = "bold";
		barsMonth[i].style.width = per * 100 + "%"
		barsMonth[i].innerHTML = "M:" + (per * 100).toFixed(0) + "%";
	}

	for(let i = 0; i < barsYear.length; i++){
		let per;
		let passDays = date.getDate();
		if(year % 4 == 0 && year % 100 != 0 || year % 400 == 0){
		for(let i = 0; i < month; i++){
			passDays += monthsLeap[i]
		}
			per = passDays / 366
		} else {
		for(let i = 0; i < month; i++){
			passDays += monthsCommon[i]
		}
			per = passDays / 365
		}
		if(per < 0.25){
			barsYear[i].style.backgroundImage = greenBG;
		} else if(per < 0.5){
			barsYear[i].style.backgroundImage = blueBG;
		} else if(per < 0.75){
			barsYear[i].style.backgroundImage = yellowBG;
		} else {
			barsYear[i].style.backgroundImage = redBG;
		}
		barsYear[i].style.fontWeight = "bold";
		barsYear[i].style.width = per * 100 + "%"
		barsYear[i].innerHTML = "Y: " + (per * 100).toFixed(0) + "%";
	}
}
```

## DIRECTION

> [!caution] 注意
> 根据自己笔记库中对于weekly review的命名规则，修改下面这个语句，让它可以自动嵌入上周的weekly review中关于本周计划的部分。

![[Weekly <% tp.date.now("YYYY-ww", -7) %>#This week]]

## GET READY

###  Morning Checklist

- [ ] 整理起居
- [ ] 充足饮水
- [ ] 晨练晨跑
- [ ] 深度思考10min
- [ ] 整理工作桌面

### Confirmations
- 

### GTD & Top 3 Tasks

> [!NOTE]+ Get Things Done
> **1. 收集**：收集所有任务、想法、计划、待办事项。
> **2. 组织**：审视待办任务，分类所有任务和行动步骤，并回顾过往未完成的项目。
> > **2.1 分类**：根据任务属性（环境Context、项目Project、状态Status、截止时间Due）分类，单独任务、父子任务、项目类属任务...
> > 
> > **2.2 回顾**：定期回顾+跟踪进度，优先级排序。
> 
> **3. 执行**：专注于当前任务，避免分散注意力，提高工作效率。

### Todo list

-[ ]
-[ ]
-[ ]
-[ ]
-[ ]



## RELATIONSHIP

> [!caution] 注意
> 根据个人需求，修改dataview中的时间，让跟进的时间间隔符合你自己的要求

### Family
 ```dataview
table without ID
file.link as "Family", date_last_spoken as "Last Time"
from #people/family 
where follow_up = true
and date_last_spoken <= date(today) - dur(2 days)
```

### Friend
```dataview
table without ID
file.link as Friend, date_last_spoken as "Last Time"
from #people/friend
where follow_up = true
and date_last_spoken <= date(today) - dur(1 week)
```
 `dice: #people/friend|link`
 
### Client
```dataview
table without id file.link as Client, date_last_spoken as "Last Time"
from #people/client 
where follow_up = true
and date_last_spoken <= date(today) - dur(2 week)
```
 `dice: #people/client|link`
 
## REVIEW
### Go Back To The Future

> [!caution] 注意
> 把标签换成你日记的标签就可以了

 `dice: #review/daily|link`
### What happened today?
#### Project

> [!important] Prompt
> 今天关于项目的内容，请按照以下步骤进行复盘: 
> 1.回顾目标 2.叙述过程（5W1H）3.评估结果（SWOT）4.分析原因 （5WHYs） 5.推演规律  6.记录归档 

*Achivement*

*Opportunity*

*Action Plan*


#### About Today

 *win*

*struggle*

*other*


#### Idea


### Be Grateful!
- 

## END-OF-DAY CHECKLIST
- [ ] GTD
- [ ] bookkeeping
- [ ] review bookmarks
- [ ] check [[Habit Tracker]]
- [ ] Back Up
	- [ ] Time Machine
	- [ ] Obsidian Vault
- [ ] clean up the photos and videos
- [ ] check e-mail inbox

## NOTES

> [!caution] 注意
> 这边dataview报错不用担心，因为我在中间写了一句templater的语句，套用模板的时候会自动变成当天日期，这个dataview语句就可以正常运作了
### Notes created today
```dataview
list
where file.cday = date(<% tp.file.creation_date("YYYY-MM-DD") %>)
sort file.ctime asc
```
### Notes modified today
```dataview
list
where file.mday = date(<% tp.file.creation_date("YYYY-MM-DD") %>)
sort file.mtime asc
```

## HABIT TRACKER

> [!caution] 注意
> dataviewjs中需要修改的位置，已经在代码备注中用中文注明了

```dataviewjs
dv.span("**Habit_1**")  // 这里需要修改
const calendarData = {
    year: 2024,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages('"daily"').where(p => p.Habit_1)) {
    //dv.span("<br>" + page.file.name) 这里需要修改// uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        intensity: page.Habit_1, // (required) the data you want to track, will map color intensities automatically 这里需要修改
        content: "",           // (optional) Add text to the date cell
        color: "orange",          // (optional) Reference from 这里改成自己需要的颜色*calendarData.colors*. If no color is supplied; colors[0] is used
    })
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Habit_2**") 
const calendarData = {
    year: 2024,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages('"daily"').where(p => p.Habit_2)) {
    //dv.span("<br>" + page.file.name) // uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        intensity: page.Habit_2, // (required) the data you want to track, will map color intensities automatically
        content: "",           // (optional) Add text to the date cell
        color: "pink",          // (optional) Reference from *calendarData.colors*. If no color is supplied; colors[0] is used
    })
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Habit_3**") 
const calendarData = {
    year: 2024,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages('"daily"').where(p => p.Habit_3)) {
    //dv.span("<br>" + page.file.name) // uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        intensity: page.Habit_3, // (required) the data you want to track, will map color intensities automatically
        content: "",           // (optional) Add text to the date cell
        color: "blue",          // (optional) Reference from *calendarData.colors*. If no color is supplied; colors[0] is used
    })
}

renderHeatmapCalendar(this.container, calendarData)
```
```dataviewjs
dv.span("**Habit_4**") 
const calendarData = {
    year: 2024,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages('"daily"').where(p => p.Habit_4)) {
    //dv.span("<br>" + page.file.name) // uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        intensity: page.Habit_4, // (required) the data you want to track, will map color intensities automatically
        content: "",           // (optional) Add text to the date cell
        color: "green",          // (optional) Reference from *calendarData.colors*. If no color is supplied; colors[0] is used
    })
}

renderHeatmapCalendar(this.container, calendarData)
```
