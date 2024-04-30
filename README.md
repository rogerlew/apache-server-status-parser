# apache_server_status 

**`apache_server_status`** is a Python module to fetch and 
parse the Apache HTTP Server status page, focusing specifically 
on servers utilizing the MPM_Event module. 

This script retrieves data from the server status page, 
parses HTML content to extract key server metrics, and 
converts these metrics into various data types like integers, 
floats, and ISO-formatted dates for easy analysis and monitoring.

**Keywords**: apache, apache2, httpd, server-status, server-status scrapping, server-status to json, server-status parser

## Features

- Fetch and parse server status from any Apache server running the MPM_Event module.
- Extract and convert server metrics to appropriate data types.
- Handle server status pages efficiently, parsing specific sections for crucial statistics.

## Installation

Clone the repository within your site-packages:

```bash
git clone https://github.com/rogerlew/ApacheStatusParser.git
```

## Usage

```python
After installation, use the module to get server status as follows:
>>> from pprint import pprint
>>> import apache_server_status
>>> stats = apache_server_status.get_server_status()
>>> pprint(stats)
{'CPU Usage': 'u27.55 s14 cu0 cs0',
 'CPU load': '.102%',
 'Current Time': '2024-04-30T17:10:33+00:00',
 'Parent Server Config. Generation': 3,
 'Parent Server MPM Generation': 2,
 'Restart Time': '2024-04-30T05:52:06+00:00',
 'Server Built': '2023-03-09T01:34:33+00:00',
 'Server MPM': 'event',
 'Server Version': 'Apache/2.4.29 (Ubuntu) OpenSSL/1.1.1 mod_wsgi/4.5.17',
 'Server load': '2004-03-03T08:00:00+00:00',
 'Server uptime': '2024-04-30T18:18:27+00:00',
 'Total Traffic': '319.7 MB',
 'Total accesses': 7955,
 'idle workers': 60,
 'kB/request': 41.2,
 'requests currently being processed': 15,
 'requests/sec': 0.195}
>>>
```


## License

This project is released into the public domain under The Unlicense. For more details, see the [LICENSE](LICENSE) file.

