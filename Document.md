# Include 'PHP\_TimeTable.php' file #

```
include_once('src/PHP_TimeTable.php');
```

# Create TimeTable #

```
$timetable = new TimeTable();
```

### Set Start-End time of TimeTable ###

$timetable->setTime(**Start\_Time**,**End\_Time**);

**example**
```
$timetable->setTime("7:00","12:00");
```

### Set rate time ###

$timetable->setTimeRate(**Minute**);

**example**
```
$timetable->setTimeRate(30);
```

### Set Text ###

$timetable->setText(**Text**);

**example**
```
$timetable->setText("Day/Time");
```

### Set Option Text ###

$timetable->setOptionText(**Text**);

**example**
```
$timetable->setOptionText("Option");
```

### Set Empty Text ###

$timetable->setOptionText(**Text**,**HTML\_Attribute**);

**example**
```
$timetable->setEmpty("empty",'class="empty"');
```

### Set Table Attribute ###

$timetable->setStyle(**HTML\_Attribute**);

**example**
```
$timetable->setStyle('border="1" cellpadding=5 cellspacing=0');
```



---



# Create Day #

$day1 = new TableDay(**Name**,**Day\_HTML\_Attribute**,**Book\_Text**,**Book\_URL**,**Book\_HTML\_Attribute**);

**example**
```
$day1 = new TableDay('Day 1','','Book This','book.php?day=1');
```


# Add Times To Day #

$day1->addTime(**Start\_Time**,**End\_Time**,**Text**,**Time\_HTML\_Attribute**,**URL**,**URL\_HTML\_Attribute**);

**example**
```
$day1->addTime('7:00','8:00','Wait','style="background-color:#EEE"','#');
$day1->addTime('9:00','10:00','Booked','style="background-color:#FF0"','#');
```

# Add Day to TimeTable #

$timetable->addDay(**TableDay**);

**example**
```
$timetable->addDay($day2);
```

# Create TimeTable #

$timetable->create();

**example**
```
echo $timetable->create();
```