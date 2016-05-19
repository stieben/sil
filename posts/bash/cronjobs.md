# Cronjobs

_#unix_ _#bash_ _#automation_

Cronjobs are tasks that are triggered by the system and thus performed automatically at specific times.
Cronjobs are managed inside a text file called _crontab_.

## List existing cronjobs

```bash
crontab -l
```

## Edit crontab

```bash
crontab -e
```

## Syntax

Each line of the crontab defines a task.
The structure of each line looks like this:

```
* * * * * /path/to/script.sh
```

The asterisks stand for, respectively:

1. Minute (0-59)
2. Hour (0-23)
3. Day of the month (1-31)
4. Month (1-12)
5. Day of the week (0-7) (Sunday is either 0 or 7)

### Examples

Every minute:

```
* * * * * /path/to/script.sh
```

Every 5 minutes:

```
*/5 * * * * /path/to/script.sh
```

Monday to Friday at 10:30 PM:

```
30 22 * * 1,2,3,4,5 /path/to/script.sh
```

Every half an hour, between 8 AM and 8 PM:

```
30 8-20 * * * /path/to/script.sh
```

Every day at 8:15 PM, with two parameters for the script:

```
15 20 * * * /path/to/script.sh param1 param2
```

### Aliases

| Alias                    | Replacement  |
| ------------------------ | ------------ |
| _@hourly_                | `0 * * * *`  |
| _@daily_ or _@midnight_  | `0 0 * * *`  |
| _@weekly_                | `0 0 * * 0`  |
| _@monthly_               | `0 0 1 * *`  |
| _@yearly_ or _@annually_ | `0 0 1 1 *`  |
| _@reboot_                | After reboot |

So you can also write your cronjob like this:

```
@daily /path/to/script.sh
```

## Credits

Information taken from [Uberspace Wiki](https://wiki.uberspace.de/system:cron).
