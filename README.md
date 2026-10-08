# FTP server to transfer files between machines with zero configuration
## Usage
0. Create and enable virtualenvironment
`python -m venv env; source env/bin/activate`

2. Install module
`python -m pip install python-ftp-server`

3. Run the FTP server
`ftp_server -d "directory/to/share"`

or equivalently:
`python -m python_ftp_server -d "directory/to/share"`

will print:
```bash
Local address: ftp://<IP>:60000
User: <USER>
Password: <PASSWORD>
```

Connect with ftp client

Copy and paste your `IP`, `USER`, `PASSWORD`, `PORT` into [FileZilla](https://filezilla-project.org/) (or any other FTP client):
![](https://github.com/Red-Eyed/python_ftp_server/raw/master/img.png)

- aria2c
- curl

## Options

| Option | Default | Description |
| --- | --- | --- |
| `-u`, `--user` | `user` | Username |
| `-p`, `--password` | random 20 chars | Password |
| `-r`, `--readonly` | off | Serve files read-only |
| `-d`, `--dir` | current directory | Directory to share |
| `--ip` | local IP | Address to bind |
| `--port` | `60000` | Control port |
| `--port_range` | `60001-60100` | Passive data port range |
| `--tls` | off | Require FTPS (TLS) with a self-signed cert |

Example with TLS:
`ftp_server -d /tmp --tls`

