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

```python
from datetime import datetime

dt = datetime.now()

print(dt.strftime('%a'))
```

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


```python
import re

pattern = 'this'
text = 'Does this text match the pattern?'

match = re.search(pattern, text)
```

#### Phone Number

`^[\+]?[(]?[0-9]{3}[)]?[-\s\.]?[0-9]{3}[-\s\.]?[0-9]{4,6}$`

#### Date

`(?:(?:31(\/|-|\.)(?:0?[13578]|1[02]))\1|(?:(?:29|30)(\/|-|\.)(?:0?[13-9]|1[0-2])\2))(?:(?:1[6-9]|[2-9]\d)?\d{2})$|^(?:29(\/|-|\.)0?2\3(?:(?:(?:1[6-9]|[2-9]\d)?(?:0[48]|[2468][048]|[13579][26])|(?:(?:16|[2468][048]|[3579][26])00))))$|^(?:0?[1-9]|1\d|2[0-8])(\/|-|\.)(?:(?:0?[1-9])|(?:1[0-2]))\4(?:(?:1[6-9]|[2-9]\d)?\d{2})`

#### IPv4 Address

`(\b25[0-5]|\b2[0-4][0-9]|\b[01]?[0-9][0-9]?)(\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)){3}`

#### IPv6 Address

`(([0-9a-fA-F]{1,4}:){7,7}[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,7}:|([0-9a-fA-F]{1,4}:){1,6}:[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,5}(:[0-9a-fA-F]{1,4}){1,2}|([0-9a-fA-F]{1,4}:){1,4}(:[0-9a-fA-F]{1,4}){1,3}|([0-9a-fA-F]{1,4}:){1,3}(:[0-9a-fA-F]{1,4}){1,4}|([0-9a-fA-F]{1,4}:){1,2}(:[0-9a-fA-F]{1,4}){1,5}|[0-9a-fA-F]{1,4}:((:[0-9a-fA-F]{1,4}){1,6})|:((:[0-9a-fA-F]{1,4}){1,7}|:)|fe80:(:[0-9a-fA-F]{0,4}){0,4}%[0-9a-zA-Z]{1,}|::(ffff(:0{1,4}){0,1}:){0,1}((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])|([0-9a-fA-F]{1,4}:){1,4}:((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9]))`

#### Email Address

`[^@ \t\r\n]+@[^@ \t\r\n]+\.[^@ \t\r\n]+`

#### Social Security Number

`^(?!0{3})(?!6{3})[0-8]\d{2}-(?!0{2})\d{2}-(?!0{4})\d{4}$`

#### Hashtag

`^#[^ !@#$%^&*(),.?":{}|<>]*$`

#### Credit Card Number

`(^4[0-9]{12}(?:[0-9]{3})?$)|(^(?:5[1-5][0-9]{2}|222[1-9]|22[3-9][0-9]|2[3-6][0-9]{2}|27[01][0-9]|2720)[0-9]{12}$)|(3[47][0-9]{13})|(^3(?:0[0-5]|[68][0-9])[0-9]{11}$)|(^6(?:011|5[0-9]{2})[0-9]{12}$)|(^(?:2131|1800|35\d{3})\d{11}$)`

#### Emoji

`(\u00a9|\u00ae|[\u2000-\u3300]|\ud83c[\ud000-\udfff]|\ud83d[\ud000-\udfff]|\ud83e[\ud000-\udfff])`

#### Bitcoin Address

`^(bc1|[13])[a-zA-HJ-NP-Z0-9]{25,39}$`

#### MAC Address

`^[a-fA-F0-9]{2}(:[a-fA-F0-9]{2}){5}$`

#### Latitude and Longitude

`^((\-?|\+?)?\d+(\.\d+)?),\s*((\-?|\+?)?\d+(\.\d+)?)$`

#### UUID

`^[0-9a-fA-F]{8}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{12}$`

#### Email \(Simple\)

`[^@ \t\r\n]+@[^@ \t\r\n]+\.[^@ \t\r\n]+`

#### Email \(Complex\)

`(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))`

#### Twitter Handle

`\b[@]?[A-Za-z0-9_]{1,15}\b`

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
