# Mail CR
Automatically send CR emails given URLs.

## Requirements
- Python 3
- Jinja 2

## Config
You need to create a `config.py` file in `src/mailer`. The file should define the following constants :

```python
SENDER = 'your@email.com'
USERNAME = 'username@email.com'
DEST_BURO = 'buro@email.com'
DEST_CA = 'ca@email.com'
PWD = 'yourS3cr3tp4ssw0rd'
SERVER = 'smtp.email.com'
PORT = 587
TLS = True
```

## Usage
```bash
python3 src/mailer/main.py -u http://example.com/teams/ca/cr.pdf http://example.com/teams/ca/cr2.pdf http://example.com/teams/bureau/cr.pdf
```
In this example, the script will send two mails : one for the CA with two CR, and one for the Buro with one CR.

Files must respect the following naming convention :
```
YYYY_MM_DD_CA_CR.pdf
YYYY_MM_DD_BUREAU_CR.pdf
```

## Licence

[![GNU GPL v3.0](http://www.gnu.org/graphics/gplv3-127x51.png)](http://www.gnu.org/licenses/gpl.html)

```
Send CR - Send mail for CR review.
Copyright (C) 2016 Gabriel AUGENDRE

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
```
