# check_certificate_expiry
Monitor a webserver certificate for its expiry date.

## Usage
```
  Usage: cce [OPTIONS]
  [OPTIONS]
  -u URL             URL
  -p PORT            Port (default: 443)
  -w WARNING         Days left threshold for warning (default: 5)
  -c CRITICAL        Days left threshold for critical (default: 1)
  -o Output Only     Only returns days left
```

## Example
```
./cce.sh -u zgheb.com -w 10 -c 5
OK: Certificate still valid for 75 days
```

```
./cce.sh -u old.zgheb.com -w 20 -c 10
WARNING: Certificate is only valid for another 18 days
```
