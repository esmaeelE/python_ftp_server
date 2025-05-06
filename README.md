# FTP server to transfer files between machines with zero configuration
## Usage
0. Create and enable virtualenvironment
`python -m venv env; source env/bin/activate`

2. Install module
`python -m pip install python-ftp-server`

3. Run python ftp server module in command line
`python -m python_ftp_server -d "dirctory/to/share"`

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

