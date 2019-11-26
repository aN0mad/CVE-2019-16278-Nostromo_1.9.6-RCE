# CVE-2019-16278 - Nostromo 1.9.6 RCE
Python script to exploit RCE in Nostromo nhttpd &lt;= 1.9.6.


## Help
```
usage: CVE-2019-16278.py [-h] [-t TARGET] [-p PORT] [-c COMMAND] [-b BYTES]

Exploit for CVE-2019-16278 - Nostromo 1.9.6 RCE

optional arguments:
  -h, --help            show this help message and exit
  -t TARGET, --target TARGET
                        Remote host to target
  -p PORT, --port PORT  Remote port to target
  -c COMMAND, --command COMMAND
                        Command to execute on the server
  -b BYTES, --bytes BYTES
                        The number of bytes to receive back in the response
```

## Usage

Run the exploit

```bash
python CVE-2019-16278.py -t 10.10.10.10. -p 80 -c whoami
```

Run the exploit and recieve more bytes in the response

```bash
python CVE-2019-16278.py -t 10.10.10.10. -p 80 -c whoami -b 4096
```

