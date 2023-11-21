# Datetime reference

How to convert text to date & time with our functions.

Parsing and formatting date & time is a common part of data preparation. This guide will show you how use the Gyana functions `parse_date`, `parse_time`, `parse_datetime` and `format_datetime`.

## Parsing

If you have date & time information stored in a text column, you'll need to use a **parsing** function to extract it.

💡 The column type is displayed by an icon in the header. You can hover over it to view the full type name.

You'll need to tell the parser how to parse the text with a format string. Here are a few examples:

    parse_date('2022-03-22', '%Y-%m-%d')parse_time('20:10:03', '%T')parse_datetime('Tuesday 22 March 2022 at 09:30', '%A %e %B %G at %R')

## Formatting

Formatting is the opposite of parsing - you have a date & time column, and you'd like to display a text representation of it.

Just as with parsing, you'll need to tell the formatter how to format the text with a format string. Here are a few examples:

    format_datetime(datetime_col, '%Y-%m-%d') # e.g. 2022-03-22format_datetime(datetime_col, '%T') # e.g. 20:10:03format_datetime(datetime_col, '%A %e %B %G at %R') # e.g. Tuesday 22 March 2022 at 09:30 

## Format string reference

You can build your format string with the reference below. **Any issues?** Reach out to support.

Format element

Description

Example

%A

The full weekday name.

Wednesday

%a

The abbreviated weekday name.

Wed

%B

The full month name.

January

%b

The abbreviated month name.

Jan

%C

The century (a year divided by 100 and truncated to an integer) as a decimal number (00-99).

20

%c

The date and time representation.

Wed Jan 20 21:47:00 2021

%D

The date in the format %m/%d/%y.

01/20/21

%d

The day of the month as a decimal number (01-31).

20

%e

The day of month as a decimal number (1-31); single digits are preceded by a space.

20

%F

The date in the format %Y-%m-%d.

2021-01-20

%G

The ISO 8601 year with century as a decimal number. Each ISO year begins on the Monday before the first Thursday of the Gregorian calendar year. Note that %G and %Y may produce different results near Gregorian year boundaries, where the Gregorian year and ISO year can diverge.

2021

%g

The ISO 8601 year without century as a decimal number (00-99). Each ISO year begins on the Monday before the first Thursday of the Gregorian calendar year. Note that %g and %y may produce different results near Gregorian year boundaries, where the Gregorian year and ISO year can diverge.

21

%H

The hour (24-hour clock) as a decimal number (00-23).

21

%h

The abbreviated month name.

Jan

%I

The hour (12-hour clock) as a decimal number (01-12).

09

%j

The day of the year as a decimal number (001-366).

020

%k

The hour (24-hour clock) as a decimal number (0-23); single digits are preceded by a space.

21

%l

The hour (12-hour clock) as a decimal number (1-12); single digits are preceded by a space.

9

%M

The minute as a decimal number (00-59).

47

%m

The month as a decimal number (01-12).

01

%n

A newline character.

%P

Either am or pm.

pm

%p

Either AM or PM.

PM

%Q

The quarter as a decimal number (1-4).

1

%R

The time in the format %H:%M.

21:47

%S

The second as a decimal number (00-60).

00

%s

The number of seconds since 1970-01-01 00:00:00. Always overrides all other format elements, independent of where %s appears in the string. If multiple %s elements appear, then the last one takes precedence.

1611179220

%T

The time in the format %H:%M:%S.

21:47:00

%t

A tab character.

%U

The week number of the year (Sunday as the first day of the week) as a decimal number (00-53).

03

%u

The weekday (Monday as the first day of the week) as a decimal number (1-7).

3

%V

The ISO 8601 week number of the year (Monday as the first day of the week) as a decimal number (01-53). If the week containing January 1 has four or more days in the new year, then it is week 1; otherwise it is week 53 of the previous year, and the next week is week 1.

03

%W

The week number of the year (Monday as the first day of the week) as a decimal number (00-53).

03

%w

The weekday (Sunday as the first day of the week) as a decimal number (0-6).

3

%X

The time representation in HH:MM:SS format.

21:47:00

%x

The date representation in MM/DD/YY format.

01/20/21

%Y

The year with century as a decimal number.

2021

%y

The year without century as a decimal number (00-99), with an optional leading zero. Can be mixed with %C. If %C is not specified, years 00-68 are 2000s, while years 69-99 are 1900s.

21

%Z

The time zone name.

UTC-5

%z

The offset from the Prime Meridian in the format +HHMM or -HHMM as appropriate, with positive values representing locations east of Greenwich.

\-0500

%%

A single % character.

%

%Ez

RFC 3339-compatible numeric time zone (+HH:MM or -HH:MM).

\-05:00

%E<number>S

Seconds with <number> digits of fractional precision.

00.000 for %E3S

%E\*S

Seconds with full fractional precision (a literal '\*').

00.123456

%E4Y

Four-character years (0001 ... 9999). Note that %Y produces as many characters as it takes to fully render the year.

2021