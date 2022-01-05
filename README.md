# Get datetime based on area Timezone  in php 
In this repo, you will get "How do I get the current date and time in PHP based on zone ?" 


# some script that provide month last date ,  week last date

```php

$week_start = strtotime('last Sunday', time());
$week_end = strtotime('next Sunday', time());

$month_start = strtotime('first day of this month', time());
$month_end = strtotime('last day of this month', time());

$year_start = strtotime('first day of January', time());
$year_end = strtotime('last day of December', time());

echo date('D, M jS Y', $week_start).'<br/>';
echo date('D, M jS Y', $week_end).'<br/>';

echo date('D, M jS Y', $month_start).'<br/>';
echo date('D, M jS Y', $month_end).'<br/>';

echo date('D, M jS Y', $year_start).'<br/>';
echo date('D, M jS Y', $year_end).'<br/>';
```



# Get current month date   and get after 2 month last date 

```mysql
`date_submitted` BETWEEN  DATE_FORMAT(NOW() ,'%Y-%m-01') AND LAST_DAY(DATE(NOW()) + INTERVAL 2 MONTH) 
```

# For this Code are : 

```php
$timezone_name = date_default_timezone_get();


date_default_timezone_set('Australia/Melbourne');
$date = date('m/d/Y h:i:s a', time());



$timezone_offset_minutes = 330;
$timezone_name = timezone_name_from_abbr("", $timezone_offset_minutes*60, false);

$date = new DateTime('now', new DateTimeZone($timezone_name));
 echo $date->format('d-m-Y h:i:s'); 

```


# If you get date from excel file then you have to apply these solution  (date is short date)

```html
Please use this formula to change from Excel date to Unix date, then you can use "gmdate" to get the real date in PHP:

UNIX_DATE = (EXCEL_DATE - 25569) * 86400
and to convert from Unix date to Excel date, use this formula:

EXCEL_DATE = 25569 + (UNIX_DATE / 86400)
After putting this formula into a variable, you can get the real date in PHP using this example:

$UNIX_DATE = ($EXCEL_DATE - 25569) * 86400;
echo gmdate("d-m-Y H:i:s", $UNIX_DATE);
```
