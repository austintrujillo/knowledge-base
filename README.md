# Knowledge Base

- [Date & Time Patterns](https://github.com/austintrujillo/knowledge-base/edit/main/README.md#date--time-patterns)
  - [Standards](https://github.com/austintrujillo/knowledge-base/edit/main/README.md#standards)
  - [Time](https://github.com/austintrujillo/knowledge-base/edit/main/README.md#time-patterns)
  - [Date](https://github.com/austintrujillo/knowledge-base/edit/main/README.md#date)
  - [Miscellaneous](https://github.com/austintrujillo/knowledge-base/edit/main/README.md#miscellaneous)

- [Regex Patterns](https://github.com/austintrujillo/knowledge-base/edit/main/README.md#regex-patterns)

- [Dimensions]()

- [Temperature Conversions](https://github.com/austintrujillo/knowledge-base/edit/main/README.md#temperature-conversions)
  - [Fahrenheit to Celsius](https://github.com/austintrujillo/knowledge-base/edit/main/README.md#fahrenheit-to-celsius)
  - [Celsius to Fahrenheit](https://github.com/austintrujillo/knowledge-base/edit/main/README.md#celsius-to-fahrenheit)

---

## Date & Time Patterns

#### Standards
| Example | Pattern Name |
| ----------- | ----------- |
| 5/29/1994 12:00 | Short|
| May 29, 1994 at 12:00:00 | Medium |
| May 29, 1994 at 12:00:00 MDT | Long |
| Mon, 29 May 1994 12:00:00 -0600 | RFC 2822 |
| 1994-05-29T12:00:00-0600 | ISO 8601 |

#### Time
| Pattern | Example | Description |
| ----------- | ----------- | ----------- |
| F | 0-9 | Most significant digit of fractional seconds. Nothing is displayed if zero |
| f | 0-9 | Most significant digit of fractional seconds |
| ff | 0-99 | Two most significant digit of fractional seconds |
| fff | 0-999 | Three most significant digit of fractional seconds |
| ffff | 0-9999 | Four most significant digit of fractional seconds |
| fffff | 0-99999 | Five most significant digit of fractional seconds |
| ffffff | 0-999999 | Six most significant digit of fractional seconds |
| fffffff | 0-9999999 | Seven most significant digit of fractional seconds |
| s | 0-59 | Seconds |
| ss | 00-59 | Seconds with a leading zero |
| m | 0-59 | Minutes |
| mm | 00-59 | Minutes with a leading zero |
| h | 1-12 | 12-hour clock hour |
| hh | 01-12 | 12-hour clock hour with leading zero |
| H | 0-24 | 24-hour clock hour |
| hh | 00-24 | 24-hour clock hour with leading zero |
| t | A,P | Abbreviated AM/PM |
| tt | AM,PM | AM/PM |

#### Date
| Pattern | Example | Description |
| ----------- | ----------- | ----------- |
| d | 1-31 | Day of the month as a number |
| dd | 01-31 | Day of the month as a number with a loading zero |
| ddd | Mon, Tues, Wed etc. | Abbreviated name of the day of the week |
| dddd | Monday, Tuesday, Wednesday, etc. | Full name of the day of the week |
| M | 1-12 | Month number |
| MM | 01-12 | Month number with leading zero |
| MMM | Jan, Feb, Mar, etc. | Abbreviated month name |
| MMMM | January, February, March, etc. | Full month name |
| y | 0-99 | Year (eg. 2001 = 1) |
| yy | 00-99 | Year with leading zero (eg. 2001 = 01) |
| yyy | 2001, 2002, 2003, etc. | Year |
| yyyy | 2001, 2002, 2003, etc. | Year |
| K | +05:00, +06:00, +07:00, etc. | Time zone information |
| z | +6,+7,+8, etc. | Offset from UTC |
| zz | +06,+07,+08, etc. | Offset from UTC with leading zero |
| zzz | +06:00, +07:00, +08:00, etc.  | Offset from UTC represented in hours |

#### Miscellaneous

| Pattern | Example | Description |
| ----------- | ----------- | ----------- |
| : | 12:43:27 | Time separator for hours, minutes, and seconds |
| / | 05/29/1994 | Date separator for months, days, and years |
| " | 12"+"43"+"27 | Displays the literal character. The application should escape the quotation marks with a backslash ( \ ) |
| '' | 12''+''43''+''27 | Double single quote displays the literal character |

## Regex Patterns

## Temperature Conversions

#### Fahrenheit to Celsius

##### Basic Conversion
`°C = (°F - 30) / 2`

##### Advanced Conversion
`°C = (°F - 32) * 5 / 9`

##### Conversion Table
| °F | °C |
|------|------|
| 5° F | -15° C |
| 14° F | -10° C |
| 23° F | -5° C |
| 32° F | 0° C |
| 41° F | 5° C |
| 50° F | 10° C |
| 59° F | 15° C |
| 68° F | 20° C |
| 77° F | 25° C |
| 86° F | 30° C |
| 95° F | 35° C |
| 104° F | 40° C |
| 113° F | 45° C |
| 122° F | 50° C |
| 131° F | 55° C |
| 140° F | 60° C |
| 149° F | 65° C |
| 158° F | 70° C |
| 167° F | 75° C |
| 176° F | 80° C |
| 185° F | 85° C |
| 194° F | 90° C |
| 203° F | 95° C |
| 212° F | 100° C | 

#### Celsius to Fahrenheit

##### Basic Conversion
`°F = (°C * 2) + 30`

##### Advanced Conversion
`°F = (°C * (9/5)) + 32`

##### Conversion Table
| °C | °F |
|------|------|
| -15° C | 5° F |
| -10° C | 14° F |
| -5° C | 23° F |
| 0° C | 32° F |
| 5° C | 41° F |
| 10° C | 50° F |
| 15° C | 59° F |
| 20° C | 68° F |
| 25° C | 77° F |
| 30° C | 86° F |
| 35° C | 95° F |
| 40° C | 104° F |
| 45° C | 113° F |
| 50° C | 122° F |
| 55° C | 131° F |
| 60° C | 140° F |
| 65° C | 149° F |
| 70° C | 158° F |
| 75° C | 167° F |
| 80° C | 176° F |
| 85° C | 185° F |
| 90° C | 194° F |
| 95° C | 203° F |
| 100° C | 212° F |
