# Global Object Application       


### GOA_GetFirstDayOfMonth
- Exprsssion Rule                    

        text(
        date(year(ri!date, ), month(ri!date), 1),
        "dddd"
        )

### GOA_FirstDaySunday
**Accepts a date of a month that starts on Sunday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule  

        a!match(
        value:daysinmonth(month( ri!date ), year(ri!date)),
        equals: 28,
        then: {
            a!map(weekDay: "Sunday", day1: 1, day2: 8, day3: 15, day4: 22, day5: null, day6: null),
            a!map(weekDay: "Monday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Tuesday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Wednesday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 6, day2: 13, day3: 20, day4: 27, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 7, day2: 14, day3: 21, day4: 28, day5: null, day6: null)
        },
        equals: 29,
        then:  {
            a!map(weekDay: "Sunday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Monday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Tuesday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Wednesday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 6, day2: 13, day3: 20, day4: 27, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 7, day2: 14, day3: 21, day4: 28, day5: null, day6: null)
        },
        equals: 30,
        then: {
            a!map(weekDay: "Sunday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Monday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Tuesday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Wednesday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 6, day2: 13, day3: 20, day4: 27, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 7, day2: 14, day3: 21, day4: 28, day5: null, day6: null)
        },
        default: {
            a!map(weekDay: "Sunday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Monday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Tuesday", day1: 3, day2: 10, day3: 17, day4: 24, day5: 31, day6: null),
            a!map(weekDay: "Wednesday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 6, day2: 13, day3: 20, day4: 27, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 7, day2: 14, day3: 21, day4: 28, day5: null, day6: null)
        },
        )

----
### GOA_FirstDayMonday
**Accepts a date of a month that starts on Monday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule 

        a!match(
        value:daysinmonth(month( ri!date ), year(ri!date)),
        equals: 28,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Monday", day1: 1, day2: 8, day3: 15, day4: 22, day5: null, day6: null),
            a!map(weekDay: "Tuesday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Wednesday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 6, day2: 13, day3: 20, day4: 27, day5: null, day6: null)
        },
        equals: 29,
        then:  {
            a!map(weekDay: "Sunday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Monday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Tuesday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Wednesday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 6, day2: 13, day3: 20, day4: 27, day5: null, day6: null)
        },
        equals: 30,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Monday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Tuesday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Wednesday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 6, day2: 13, day3: 20, day4: 27, day5: null, day6: null)
        },
        default: {
            a!map(weekDay: "Sunday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Monday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Tuesday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Wednesday", day1: 3, day2: 10, day3: 17, day4: 24, day5: 31, day6: null),
            a!map(weekDay: "Thursday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 6, day2: 13, day3: 20, day4: 27, day5: null, day6: null)
        },
        )
----

### GOA_FirstDayTuesday
**Accepts a date of a month that starts on Tuesday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule

        a!match(
        value:daysinmonth(month( ri!date ), year(ri!date)),
        equals: 28,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Tuesday", day1: 1, day2: 8, day3: 15, day4: 22, day5: null, day6: null),
            a!map(weekDay: "Wednesday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null)
        },
        equals: 29,
        then:  {
            a!map(weekDay: "Sunday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Tuesday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Wednesday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null)
        },
        equals: 30,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Tuesday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Wednesday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Thursday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null)
        },
        default: {
            a!map(weekDay: "Sunday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Tuesday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Wednesday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Thursday", day1: 3, day2: 10, day3: 17, day4: 24, day5: 31, day6: null),
            a!map(weekDay: "Friday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 5, day2: 12, day3: 19, day4: 26, day5: null, day6: null)
        },
        )
----

### GOA_FirstDayWednesday
**Accepts a date of a month that starts on Wednesday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule

        a!match(
        value:daysinmonth(month( ri!date ), year(ri!date)),
        equals: 28,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Wednesday", day1: 1, day2: 8, day3: 15, day4: 22, day5: null, day6: null),
            a!map(weekDay: "Thursday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null)
        },
        equals: 29,
        then:  {
            a!map(weekDay: "Sunday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Wednesday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Thursday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null)
        },
        equals: 30,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Wednesday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Thursday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Friday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null)
        },
        default: {
            a!map(weekDay: "Sunday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Wednesday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Thursday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Friday", day1: 3, day2: 10, day3: 17, day4: 24, day5: 31, day6: null),
            a!map(weekDay: "Saturday", day1: 4, day2: 11, day3: 18, day4: 25, day5: null, day6: null)
        },
        )
----

### GOA_FirstDayThursday
**Accepts a date of a month that starts on Thursday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule

        a!match(
        value:daysinmonth(month( ri!date ), year(ri!date)),
        equals: 28,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 4, day3: 11, day4: 18, day5: 25, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Wednesday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Thursday", day1: 1, day2: 8, day3: 15, day4: 22, day5: null, day6: null),
            a!map(weekDay: "Friday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null)
        },
        equals: 29,
        then:  {
            a!map(weekDay: "Sunday", day1: null, day2: 4, day3: 11, day4: 18, day5: 25, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Wednesday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Thursday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Friday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null)
        },
        equals: 30,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 4, day3: 11, day4: 18, day5: 25, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Wednesday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Thursday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Friday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Saturday", day1: 3, day2: 10, day3: 17, day4: 24, day5: null, day6: null)
        },
        default: {
            a!map(weekDay: "Sunday", day1: null, day2: 4, day3: 11, day4: 18, day5: 25, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Wednesday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Thursday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Friday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null),
            a!map(weekDay: "Saturday", day1: 3, day2: 10, day3: 17, day4: 24, day5: 31, day6: null)
        },
        )
----

### GOA_FirstDayFriday
**Accepts a date of a month that starts on Friday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule

        a!match(
        value:daysinmonth(month( ri!date ), year(ri!date)),
        equals: 28,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 3, day3: 10, day4: 17, day5: 24, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 4, day3: 11, day4: 18, day5: 25, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Wednesday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Thursday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Friday", day1: 1, day2: 8, day3: 15, day4: 22, day5: null, day6: null),
            a!map(weekDay: "Saturday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null)
        },
        equals: 29,
        then:  {
            a!map(weekDay: "Sunday", day1: null, day2: 3, day3: 10, day4: 17, day5: 24, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 4, day3: 11, day4: 18, day5: 25, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Wednesday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Thursday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Friday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Saturday", day1: 2, day2: 9, day3: 16, day4: 23, day5: null, day6: null)
        },
        equals: 30,
        then: {
            a!map(weekDay: "Sunday", day1: null, day2: 3, day3: 10, day4: 17, day5: 24, day6: null),
            a!map(weekDay: "Monday", day1: null, day2: 4, day3: 11, day4: 18, day5: 25, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Wednesday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Thursday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Friday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Saturday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null)
        },
        default: {
            a!map(weekDay: "Sunday", day1: null, day2: 3, day3: 10, day4: 17, day5: 24, day6: 31),
            a!map(weekDay: "Monday", day1: null, day2: 4, day3: 11, day4: 18, day5: 25, day6: null),
            a!map(weekDay: "Tuesday", day1: null, day2: 5, day3: 12, day4: 19, day5: 26, day6: null),
            a!map(weekDay: "Wednesday", day1: null, day2: 6, day3: 13, day4: 20, day5: 27, day6: null),
            a!map(weekDay: "Thursday", day1: null, day2: 7, day3: 14, day4: 21, day5: 28, day6: null),
            a!map(weekDay: "Friday", day1: 1, day2: 8, day3: 15, day4: 22, day5: 29, day6: null),
            a!map(weekDay: "Saturday", day1: 2, day2: 9, day3: 16, day4: 23, day5: 30, day6: null)
        },
        )