# Lifegoals

A solution to support the realization of lifegoals.

A lifegoal is a rather big target. This solution shall help breaking those down in a manner that supports their realization. Here a general classification of what shall be achieved in this solution shall happen.


[[_TOC_]]

# Definitions

## Goal

A goal is a set of measurable, defined values at a defined point in time. [^1]

[^1]:

## Lifegoal

A Lifegoal in itself is rather unspecified. Even if there is a defined set of measures describing such a goal, it 

```Mermaid
    gantt
        dateFormat  YYYY
        title       Lifegoals
        excludes    weekends
        %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)
        axisFormat  %Y

        section Lifegoal I
        Lifegoal            :milestone, 2100, 0d
```

But it is a prozess

```Mermaid
    gantt
        dateFormat  YYYY
        title       Lifegoals
        excludes    weekends
        %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)
        axisFormat  %Y
        todayMarker stroke-width:5px,stroke:#0f0,opacity:0.5

        section Lifegoal I
        Now                 :milestone, done, 2022,0d
        Lifegoal            :milestone, 2100, 0d
```

Set finite timelines of max 5 years. Goals are not fixed, they may be adjusted.

```Mermaid
    gantt
        dateFormat  YYYY
        title       Lifegoals
        excludes    weekends
        %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)
        axisFormat  %Y
        todayMarker stroke-width:5px,stroke:#0f0,opacity:0.5

        section Lifegoal I
        Now                 :milestone, done, 2022,0d
        Lifegoal            :milestone, 2027, 0d
```

Do stuff in the meantime to achieve goals.

```Mermaid
    gantt
        dateFormat  YYYY
        title       Lifegoals
        %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)
        axisFormat  %Y
        todayMarker stroke-width:5px,stroke:#0f0,opacity:0.5

        section Lifegoal I
        Now                 :milestone, done, 2022,0d
        Action              :active,2022,260w
        Lifegoal            :milestone, 2027, 0d
```

Divide and Conquer

```Mermaid
    gantt
        dateFormat  YYYY
        title       Lifegoals
        %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)
        axisFormat  %Y
        todayMarker stroke-width:5px,stroke:#0f0,opacity:0.5

        section Lifegoal I
        Now                 :milestone, done, 2022,0d
        Action 1            :active,ac1,2022, 365d
        Yeargoal 1          :milestone, active,ms1,after ac1, 0d
        Action 2            : ac2, after ac1, 365d
        Yeargoal 2          :milestone,ms2,after ac2, 0d
        Action 3            : ac3, after ac2, 366d
        Yeargoal 3          :milestone,ms2,after ac3, 0d
        Action 4            : ac4, after ac3, 365d
        Yeargoal 4          :milestone,ms2,after ac4, 0d
        Action 5            : ac5, after ac4, 365d
        Yeargoal 5          :milestone,ms2,after ac5, 0d
        Lifegoal            :milestone, after ac5, 0d
```

Multiple actions may be needed to achieve one goal.

```Mermaid
    gantt
        dateFormat  MM.YYYY
        title       Yeargoal 1
        %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)
        axisFormat  %M
        todayMarker stroke-width:5px,stroke:#0f0,opacity:0.5

        section Lifegoal I
        Now                 :milestone, done, 01.2022,0d
        Action 1            :active,ac1,01.2022,28d
        Action 2            :active,ac1,05.2022,28d
        Action 3            :active,ac1,06.2022,28d
        Action 4            :active,ac1,08.2022,28d
        Action 5            :active,ac1,09.2022,28d
        Action 6            :active,ac1,10.2022,28d
        Action 7            :active,ac1,12.2022,31d
        Yeargoal 1          :milestone, active,ms1,01.2023, 0d
```

# Conclusion

There may be several layers of goals. 

```Mermaid
erDiagram
    GOAL {
        timestamp realization
        String Name
    }
    ACTION {} 
    ACTION }o--o{ GOAL : worksTowards
    GOAL ||--o{ GOAL : parent

```
