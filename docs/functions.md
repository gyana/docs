# Function reference

How to use functions within the formula node in workflows.

## abs( number )

Calculate the absolute value of a numeric value.

Arguments:

*   _number:_ a numeric scalar or column
    

## add( x, y )

Adds two numeric values together.

Arguments:

*   _x:_ a numeric scalar or column
    
*   _y:_ a numeric scalar or column
    

## and( value, ... )

Logical and operaion

Arguments:

*   _value:_ boolean scalars or columns
    

## between( value, lower, upper )

Check if value falls between the lower/upper bounds.

Arguments:

*   _value:_ a scalar or column
    
*   _lower:_ a scalar or column representing the lower bound
    
*   _upper:_ a scalar or column representing the upper bound
    

## convert( value, type )

Change the type of a value to a different data type.

Arguments:

*   _value:_ a scalar or column
    
*   _type:_ the type to convert to, accepts \`text\`, \`float\`, \`int\`, \`str\`, \`time\`, \`date\` and \`timestamp\`
    

## ceiling( number )

Round a numeric value up to the nearest integer value greater than or equal to this value.

Arguments:

*   _number:_ a numeric scalar or column
    

## coalesce( value, ... )

Returns the first non-null value from the passed arguments in left-to-right order

Arguments:

*   _value:_ scalars or columns, uses the first not null record
    

## contains( text, pattern )

Determine if text exactly contains the given pattern.

Arguments:

*   _text:_ a text scalar or column that should contain pattern
    
*   _pattern:_ a text scalar or column that should be in text
    

## date( year, month, day )

Create a date from year, month and day

Arguments:

*   _year:_ a integer scalar or column providing the year
    
*   _month:_ a integer scalar or column providing the month
    
*   _day:_ a integer scalar or column providing the day
    

## time( hour, minute, second )

Create a time from hour, minute and second

Arguments:

*   _hour:_ a integer scalar or column providing the hour
    
*   _minute:_ a integer scalar or column providing the minute
    
*   _second:_ a integer scalar or column providing the second
    

## extract\_date( date )

Get date part from a timestamp value

## day( date )

Get the day of month from a date or timestamp value

Arguments:

*   _date:_ a timestamp scalar or column
    

## day\_of\_week( date )

Get day of the week from date or timestamp, starting from 1 Sunday to 7 Saturday

Arguments:

*   _date:_ a timestamp scalar or column
    

## divide( dividend, divisor )

Divide dividend by divisor

Arguments:

*   _dividend:_ a numeric scalar or column
    
*   _divisor:_ a numeric scalar or column
    

## epoch\_seconds( timestamp )

Seconds passed since 00:00:00 UTC on 1 January 1970 also called UNIX time

Arguments:

*   _timestamp:_ a timestamp scalar or column
    

## exp( value )

Calculate exponential value

Arguments:

*   _value:_ a scalar or column
    

## find( text, searchtext )

Returns position (0 indexed) of first occurence of searchtext in text

Arguments:

*   _text:_ a text scalar or column
    
*   _searchtext:_ a text scalar or column
    

## floor( number )

Rounding down a numeric value to the greatest integer less or eqqual

Arguments:

*   _number:_ a numeric scalar or column
    

## fillnull( value, fill\_value )

Replace nulls in value with fill\_value

Arguments:

*   _value:_ a scalar or column
    
*   _fill\_value:_ a scalar or column
    

## hash( value )

Produces a cryptographic fingerprint from value using the Fingerprint64 method

Arguments:

*   _value:_ a scalar or column
    

## hour( time )

Get the hour from date or timestamp

Arguments:

*   _time:_ a time scalar or column
    

## ifelse( condition, true\_value, false\_value )

Returns the first value if condition is true if not it returns the second value

Arguments:

*   _condition:_ a condition of a boolean column, scalar or another formula
    
*   _true\_value:_ scalar or column that is return if condition is true
    
*   _false\_value:_ scalar or column that is return if condition is false
    

## isnull( value )

Check whether value is null

Arguments:

*   _value:_ a scalar or column
    

## join( delimiter, text, ... )

Concatenate text with the delimiter

Arguments:

*   _delimiter:_ a value that is used to separate the following arguments
    
*   _text:_ a text scalar or column
    

## json\_extract( json, path ) - coming soon 🚀

Extract a field inside JSON, returns text

Arguments:

*   _json:_ a text value in JSON format
    
*   _path:_ path to the desired item in the format e.g. \`$.a.b\[0\]\`
    

## left( text, nchars )

Return up to nchars characters starting from start of each text

Arguments:

*   _text:_ a text scalar or column
    
*   _nchars:_ a numeric scalar or column indicating the number of characters from left that are returned
    

## length( text )

Calculate character length from text

Arguments:

*   _text:_ a text scalar or column
    

## like( text, pattern )

Compare text with another pattern, returns True if pattern is like text

Arguments:

*   _text:_ a text scalar or column
    
*   _pattern:_ a text scalar or column
    

## ln( number )

Returns the natural logarithm of number

Arguments:

*   _number:_ a numeric scalar or column
    

## log( number, base )

Returns the logarithm with base of number

Arguments:

*   _number:_ a numeric scalar or column
    
*   _base:_ a numeric scalar or column
    

## log2( number )

Returns the logarithm with base 2 of number

Arguments:

*   _number:_ a number scalar or column
    

## log10( number )

Returns the logarithm with base 10 of number

Arguments:

*   _number:_ a numeric scalar or column
    

## lower( text )

Turns text to lowercase

Arguments:

*   _text:_ a text scalar or column
    

## lpad( text, length \[, fillchar\] )

Returns string of given length by truncating (on left) or padding (on left) original string

Arguments:

*   _text:_ a text scalar or column
    
*   _length:_ a numeric scalar or column indicating the length of the resulting text
    
*   _fillchar:_ a text scalar or column
    

## ltrim( text )

Remove white space on the left of text

Arguments:

*   _text:_ a text scalar or column
    

## millisecond( time )

Get the milliseconds from date or timestamp

Arguments:

*   _time:_ a time scalar or column
    

## minute( time )

Get the minute from date or timestamp

Arguments:

*   _time:_ a time scalar or column
    

## month( date )

Get the month from date or timestamp

Arguments:

*   _date:_ a timestamp scalar or column
    

## modulo( x, y )

Compute the modulo of x and y

Arguments:

*   _x:_ an integer scalar or column
    
*   _y:_ an integer scalar or column
    

## product( x, y )

Multiply x and y

Arguments:

*   _x:_ a numeric scalar or column
    
*   _y:_ a numeric scalar or column
    

## notnull( value )

Check whether value is null

Arguments:

*   _value:_ a scalar or column
    

## now( )

Compute the current datetime

## or( value, ... )

Logical or operaion

Arguments:

*   _value:_ boolean scalars or columns
    

## power( number, exponent )

Calculate the number to the power of exponent

Arguments:

*   _number:_ a numeric scalar or column
    
*   _exponent:_ a numeric scalar or column
    

## regex\_extract( text, pattern, index )

_👉 Read our in depth guide on regular expressions_

Returns specified index, 0 indexed, from text based on regex pattern given

Arguments:

*   _text:_ a text scalar or column
    
*   _pattern:_ a text scalar or column
    
*   _index:_ a numeric scalar or column
    

## regex\_replace( text, pattern, replace )

_👉 Read our in depth guide on regular expressions_

Replaces match found in text by regex pattern with replace text.

Arguments:

*   _text:_ a text scalar or column
    
*   _pattern:_ a text scalar or column that is being replaced by
    
*   _replace:_ a text scalar or column that replaces the pattern in text
    

## regex\_search( text, pattern )

_👉 Read our in depth guide on regular expressions_

Search regex pattern in text

Arguments:

*   _text:_ a text scalar or column
    
*   _pattern:_ a text scalar or column
    

## repeat( text, n )

Repeat text n times

Arguments:

*   _text:_ a text scalar or column
    
*   _n:_ a numeric scalar or column
    

## replace( text, pattern, replace )

Replaces each exact occurrence of pattern in text with replace

Arguments:

*   _text:_ a text scalar or column
    
*   _pattern:_ a text scalar or column
    
*   _replace:_ a text scalar or column that replaces the pattern in text
    

## reverse( text )

Reverse text character order

Arguments:

*   _text:_ a text scalar or column
    

## right( text, nchars )

Return up to nchar characters starting from end of each text.

Arguments:

*   _text:_ a text scalar or column
    
*   _nchars:_ a numeric scalar or column indicating the number of characters from right that are returned
    

## round( number, digits )

Round number to digit decimal positon

Arguments:

*   _number:_ a numeric scalar or column
    
*   _digits:_ an integer scalar or column
    

## rpad( text, length \[, fillchar\] )

Returns string of given length by truncating (on right) or padding (on right) original string

Arguments:

*   _text:_ a text scalar or column
    
*   _length:_ a numeric scalar or column
    
*   _fillchar:_ a numeric scalar or column
    

## rtrim( text )

Remove white space on the right of text

Arguments:

*   _text:_ a text scalar or column
    

## second( time )

Get the seconds from time or timestamp

Arguments:

*   _time:_ a time scalar or column
    

## sqrt( number )

Calculate the square root

Arguments:

*   _number:_ a numeric scalar or column
    

## parse\_date( value, format )

_👉 Read our in depth guide on parsing_

Creates a date from a provided text and format

Arguments:

*   _value:_ a text scalar or column in the representing a date in \`format\`
    
*   _format:_ a text scalar or column defining the date format of \`value\` e.g '%Y-%m-%d'
    

## parse\_time( value, format )

_👉 Read our in depth guide on parsing_

Creates a time from a provided text and format

Arguments:

*   _value:_ a text scalar or column in the representing a time in \`format\`
    
*   _format:_ a text scalar or column defining the time format of \`value\` e.g '%Y-%m-%d'
    

## parse\_datetime( value, format )

_👉 Read our in depth guide on parsing_

Creates a datetime from a provided text and format

Arguments:

*   _value:_ a text scalar or column in the representing a datetime in \`format\`
    
*   _format:_ a text scalar or column defining the datetime format of \`value\` e.g '%Y-%m-%d'
    

## format\_datetime( datetime, format )

_👉 Read our in depth guide on formatting_

Format timestamp into string with given format

Arguments:

*   _datetime:_ a datetime scalar or column
    
*   _format:_ determines how the resulting text is formatted
    

## trim( text )

Remove white space surrounding the text

Arguments:

*   _text:_ a text scalar or column
    

## to\_json\_string( dictionary )

Transform a dictionary to a JSON string

Arguments:

*   _dictionary:_ a dictionary column or scalar
    

## to\_timezone( datetime, timezone )

Convert a date & time to a new date & time in a different timezone

Arguments:

*   _datetime:_ a date & time scalar or column
    
*   timezone: the time zone for the new column in tz format e.g. 'US/Pacific' (see a list here)
    

## subtract( minuend, subtrahend )

Substract subtrahend from minuend

Arguments:

*   _minuend:_ a numeric scalar or column
    
*   _subtrahend:_ a numeric scalar or column
    

## subtract\_days( date, days )

Substract days from date

Arguments:

*   _date:_ a date scalar or column
    
*   _days:_ an integer scalar or column of days to subtract
    

## substitute( text, pattern \[, replace\] \[, else\] )

Replace text if with replace if pattern is equal to text optional replace with else

Arguments:

*   _text:_ a text scalar or column
    
*   _pattern:_ a text scalar or column
    
*   _replace:_ a text scalar or column
    
*   _else:_ a text scalar or column
    

## extract\_time( datetime )

Get the time from a timestamp

Arguments:

*   _datetime:_ a datetime scalar or column
    

## datetime\_seconds( seconds, unit )

Create a datetime from an integer as the number of unit since from January 1st, 1970 UTC (unix time)

Arguments:

*   _seconds:_ an integer scalar or column
    
*   _unit:_ "s" for seconds, "ms" for milliseconds, "us" for microseconds
    

## datetime\_diff( minuend, subtrahend, unit )

Get the difference between minuend and subtrahend in the given unit

Arguments:

*   _minuend:_ a datetime scalar or column
    
*   _subtrahend:_ a datetime scalar or column
    
*   _unit:_ unit of the difference e.g. "s" for seconds
    

## today( )

Compute today's date

## truncate( datetime, unit )

Zero out smaller-size units beyond indicated unit

Arguments:

*   _datetime:_ a datetime scalar or column
    
*   _unit:_ unit e.g. "s" for seconds
    

## upper( text )

Capitalize text.

Arguments:

*   _text:_ a text scalar or column
    

## weekday( date )

Gets weekday from a date

Arguments:

*   _date:_ a timestamp scalar or column
    

## year( date )

Get the year from date

Arguments:

*   _date:_ a timestamp scalar or column

