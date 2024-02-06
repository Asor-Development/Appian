# Grid Calendar
**Calender Component created with grid, that uses 1 Interface and 9 Expression Rules**

### GOA_GridCalendar
- Interface

        a!localVariables(
            local!date,
            local!calDate: if(a!isNotNullOrEmpty(local!date),
            split(local!date, "/"),
            null
            ),
            {
                a!dateField(
                label: "Date",
                labelPosition: "ABOVE",
                value: local!date,
                saveInto: local!date,
                validations: {}
                ),
                a!richTextDisplayField(
                value: a!richTextHeader(
                    text: if(a!isNullOrEmpty(local!date),
                    text(today(), "mmmm"),
                    text(date(index(local!calDate, 3), index(local!calDate, 1), index(local!calDate, 2) ), "mmmm")
                    ),
                    size: "LARGE"
                ),
                align: "CENTER"
                ),
                a!gridField(
                data: rule!GOA_GridCalendarGetMonthDetails(if(a!isNullOrEmpty(local!date),
                today(),
                date(index(local!calDate, 3), index(local!calDate, 1), index(local!calDate, 2))
            )  
                ),
                columns: {
                    a!gridColumn(
                    label: "Sunday",
                    value: fv!row.Sunday
                    ),
                    a!gridColumn(
                    label: "Monday",
                    value: fv!row.Monday
                    ),
                    a!gridColumn(
                    label: "Tuesday",
                    value: fv!row.Tuesday
                    ),
                    a!gridColumn(
                    label: "Wednesday",
                    value: fv!row.Wednesday
                    ), a!gridColumn(
                    label: "Thursday",
                    value: fv!row.Thursday
                    ),
                    a!gridColumn(
                    label: "Friday",
                    value: fv!row.Friday
                    ),
                    a!gridColumn(
                    label: "Saturday",
                    value: fv!row.Saturday
                    )
                },
                validations: {}
                )
            }
        )


---

### GOA_GetMonthDetails
- Expression Rule


---

### GOA_GetFirstDayOfMonth
- Exprsssion Rule  


---

### GOA_FirstDaySunday
**Accepts a date of a month that starts on Sunday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule 


---

### GOA_FirstDayMonday
**Accepts a date of a month that starts on Monday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule 


---

### GOA_FirstDayTuesday
**Accepts a date of a month that starts on Tuesday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule

---

### GOA_FirstDayWednesday
**Accepts a date of a month that starts on Wednesday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule


---

### GOA_FirstDayThursday
**Accepts a date of a month that starts on Thursday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule


---

### GOA_FirstDayFriday
**Accepts a date of a month that starts on Friday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule

        a!match(
            value:daysinmonth(month( ri!date ), year(ri!date)),
            equals: 28,
            then: {
                a!map(Sunday: null, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: 1, Saturday: 2),
                a!map(Sunday: 3, Monday: 4, Tuesday: 5, Wednesday: 6, Thursday: 7, Friday: 8, Saturday: 9),
                a!map(Sunday: 10, Monday: 11, Tuesday: 12, Wednesday: 13, Thursday: 14, Friday: 15, Saturday: 16),
                a!map(Sunday: 17, Monday: 18, Tuesday: 19, Wednesday: 20, Thursday: 21, Friday: 22, Saturday: 23),
                a!map(Sunday: 24, Monday: 25, Tuesday: 26, Wednesday: 27, Thursday: 28, Friday: null, Saturday: null)
            },
            equals: 29,
            then:  {
                a!map(Sunday: null, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: 1, Saturday: 2),
                a!map(Sunday: 3, Monday: 4, Tuesday: 5, Wednesday: 6, Thursday: 7, Friday: 8, Saturday: 9),
                a!map(Sunday: 10, Monday: 11, Tuesday: 12, Wednesday: 13, Thursday: 14, Friday: 15, Saturday: 16),
                a!map(Sunday: 17, Monday: 18, Tuesday: 19, Wednesday: 20, Thursday: 21, Friday: 22, Saturday: 23),
                a!map(Sunday: 24, Monday: 25, Tuesday: 26, Wednesday: 27, Thursday: 28, Friday: 29, Saturday: null)
            },
            equals: 30,
            then: {
                a!map(Sunday: null, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: 1, Saturday: 2),
                a!map(Sunday: 3, Monday: 4, Tuesday: 5, Wednesday: 6, Thursday: 7, Friday: 8, Saturday: 9),
                a!map(Sunday: 10, Monday: 11, Tuesday: 12, Wednesday: 13, Thursday: 14, Friday: 15, Saturday: 16),
                a!map(Sunday: 17, Monday: 18, Tuesday: 19, Wednesday: 20, Thursday: 21, Friday: 22, Saturday: 23),
                a!map(Sunday: 24, Monday: 25, Tuesday: 26, Wednesday: 27, Thursday: 28, Friday: 29, Saturday: 30)
            },
            default: {
                a!map(Sunday: null, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: 1, Saturday: 2),
                a!map(Sunday: 3, Monday: 4, Tuesday: 5, Wednesday: 6, Thursday: 7, Friday: 8, Saturday: 9),
                a!map(Sunday: 10, Monday: 11, Tuesday: 12, Wednesday: 13, Thursday: 14, Friday: 15, Saturday: 16),
                a!map(Sunday: 17, Monday: 18, Tuesday: 19, Wednesday: 20, Thursday: 21, Friday: 22, Saturday: 23),
                a!map(Sunday: 24, Monday: 25, Tuesday: 26, Wednesday: 27, Thursday: 28, Friday: 29, Saturday: 30),
                a!map(Sunday: 31, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: null, Saturday:null),
            },
        )

---

### GOA_FirstDaySaturday
**Accepts a date of a month that starts on Saturday and will return a list of 7 maps, each containing a day of the week and all the dates for that day and month use with expression rule GOA_GetMonthDetails to get correct results**
- Exprsssion Rule

        a!match(
            value:daysinmonth(month( ri!date ), year(ri!date)),
            equals: 28,
            then: {
                a!map(Sunday: null, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: null, Saturday: 1),
                a!map(Sunday: 2, Monday: 3, Tuesday: 4, Wednesday: 5, Thursday: 6, Friday: 7, Saturday: 8),
                a!map(Sunday: 9, Monday: 10, Tuesday: 11, Wednesday: 12, Thursday: 13, Friday: 14, Saturday: 15),
                a!map(Sunday: 16, Monday: 17, Tuesday: 18, Wednesday: 19, Thursday: 20, Friday: 21, Saturday: 22),
                a!map(Sunday: 23, Monday: 24, Tuesday: 25, Wednesday: 26, Thursday: 27, Friday: 28, Saturday: null)
            },
            equals: 29,
            then:  {
                a!map(Sunday: null, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: null, Saturday: 1),
                a!map(Sunday: 2, Monday: 3, Tuesday: 4, Wednesday: 5, Thursday: 6, Friday: 7, Saturday: 8),
                a!map(Sunday: 9, Monday: 10, Tuesday: 11, Wednesday: 12, Thursday: 13, Friday: 14, Saturday: 15),
                a!map(Sunday: 16, Monday: 17, Tuesday: 18, Wednesday: 19, Thursday: 20, Friday: 21, Saturday: 22),
                a!map(Sunday: 23, Monday: 24, Tuesday: 25, Wednesday: 26, Thursday: 27, Friday: 28, Saturday: 29)
            },
            equals: 30,
            then: {
                a!map(Sunday: null, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: null, Saturday: 1),
                a!map(Sunday: 2, Monday: 3, Tuesday: 4, Wednesday: 5, Thursday: 6, Friday: 7, Saturday: 8),
                a!map(Sunday: 9, Monday: 10, Tuesday: 11, Wednesday: 12, Thursday: 13, Friday: 14, Saturday: 15),
                a!map(Sunday: 16, Monday: 17, Tuesday: 18, Wednesday: 19, Thursday: 20, Friday: 21, Saturday: 22),
                a!map(Sunday: 23, Monday: 24, Tuesday: 25, Wednesday: 26, Thursday: 27, Friday: 28, Saturday: 29),
                a!map(Sunday: 30, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: null, Saturday: null),
            },
            default: {
                a!map(Sunday: null, Monday: null, Tuesday: null, Wednesday: null, Thursday: null, Friday: null, Saturday: 1),
                a!map(Sunday: 2, Monday: 3, Tuesday: 4, Wednesday: 5, Thursday: 6, Friday: 7, Saturday: 8),
                a!map(Sunday: 9, Monday: 10, Tuesday: 11, Wednesday: 12, Thursday: 13, Friday: 14, Saturday: 15),
                a!map(Sunday: 16, Monday: 17, Tuesday: 18, Wednesday: 19, Thursday: 20, Friday: 21, Saturday: 22),
                a!map(Sunday: 23, Monday: 24, Tuesday: 25, Wednesday: 26, Thursday: 27, Friday: 28, Saturday: 29),
                a!map(Sunday: 30, Monday: 31, Tuesday: null, Wednesday: null, Thursday: null, Friday: null, Saturday: null),
            },
        )

---