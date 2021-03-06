# 0.0.46 (2019-9-30)

upgrade `date-fns` to `v2.4.1`
upgrade `styled-components` to `v4.4.0`

# 0.0.45 (2018-11-19)

add `typescript definitions`

# 0.0.44 (2018-11-19)

`classes` prop was extended

- `day` - class for day
- `weekDay` - class for weekDay
- `monthName` - class for monthName

# 0.0.43 (2018-11-17)

new prop:

- `firstWeekDay?: 0 | 1 | 2 | 3 | 4 | 5 | 6` - set day that will be displayed first (`0` is `sunday`)

# 0.0.42 (2018-10-24)

update styled components to `4.0.2`

# 0.0.41 (2018-09-27)

new props:

- `showMonthName: boolean` - show / hide month names
- `showWeekDayNames: boolean` - show / hide week day names
- `weekDayFormat?: string` - week day format, e.g. `E`
- `weekDayFormatter?: Date => string` - week day formatter function, e.g. `day => format(day, 'E')` (can be used to pass locale)
- `monthNameFormatter?: Date => string` - month name formatter function, e.g. `month => format(month, 'MMMM yyyy')` (can be used to pass locale)
- `width?: number` - custom base width of a single calendar (excluding margins)
- `buttonBack?: React.Node` - custom back button (will receive disabled prop)
- `buttonForward?: React.Node` - custom forwrad button (will receive disabled prop)

# 0.0.37 (2018-07-24)

- fix onClick/onHover behaviour on hidden Dates

# 0.0.36 (2018-05-29)

- new prop **CustomTd** React.ComponentType<CalendarDayProps> - shoudl be used as custom Day component in Calendar

# 0.0.35 (2018-05-17)

- new props **customClasses** { [string]: Date[]} - the class (css) will be applied to the dates that are in the array

# 0.0.34 (2018-03-23)

- **styled-components** are now `peerDependency`

# 0.0.32 (2018-03-22)

### BREAKING CHANGES

- new prop **past** - allow/disable past date selection (default `true`)
- new prop **allowedDates** - array of dates that are selectable (default `[]`) when it's empty, all dates are selectable (except disabled dates)
- new prop **rangeSelect** - if enabled, ranges can be selected, otherwise just one date (default `true`)

### BREAKING CHANGES

**numberOfMonths** and **numberOfPastMonths** were removed, use **firstMonth** and **lastMonth**

```js
numberOfMonths={1} -> firstMonth={new Date(2018, 1, 1)} // some month
numberOfPastMonths={1} -> lastMonth={new Date(2018, 2, 1)}  // some month
```
