# Get our  Timezone time in php 
In this repo, you will get "How do I get the current date and time in PHP based on zone ?" 

# For this Code are : 

```php
$timezone_offset_minutes = 330;
$timezone_name = timezone_name_from_abbr("", $timezone_offset_minutes*60, false);

$date = new DateTime('now', new DateTimeZone($timezone_name));
 echo $date->format('d-m-Y h:i:s'); 

```


# If you get date from excel file then you have top apply these solution  (date is short date)

```html
Please use this formula to change from Excel date to Unix date, then you can use "gmdate" to get the real date in PHP:

UNIX_DATE = (EXCEL_DATE - 25569) * 86400
and to convert from Unix date to Excel date, use this formula:

EXCEL_DATE = 25569 + (UNIX_DATE / 86400)
After putting this formula into a variable, you can get the real date in PHP using this example:

$UNIX_DATE = ($EXCEL_DATE - 25569) * 86400;
echo gmdate("d-m-Y H:i:s", $UNIX_DATE);
```
