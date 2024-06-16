<p align="center"><a href="https://akkupy.me"><img src="https://www.mdpi.com/sensors/sensors-21-05874/article_deploy/html/images/sensors-21-05874-g004-550.jpg" width="5000"></a></p> 

<h1 align="center"><b>BlockChain Based E-Voting System</b></h1>

* This project aims at implementing a voting system based on Blockchain technology. 
* It is a secure, transparent and decentralized way of voting.
* It converts ballots into transactions and securely mines blocks out of them.
* The advantage of a blockchain based voting system include the ability to vote from any place and prevent any tampering of votes.


# Technology stack used:
1. Python 3.11.x
2. Django Web Framework 4.2.1
3. Bootstrap 4
4. DB SQLite 3
5. HTML5

# Z-vote Production Server On Docker ([click image](https://github.com/akkupy/Z-Vote/tree/production))




# Self-hosting(Development Server)


# Open Git Cloned File
$ cd Z-Vote

# Config Virtual Env (Skip is already Done.)
$ virtualenv -p /usr/bin/python3 venv
$ . ./venv/bin/activate

# Install All Requirements.
$ pip(3) install -r requirements.txt

# Run makemigrations and migrate command.
$ python manage.py makemigrations poll
$ python manage.py migrate

# Create a Superuser.
$ python manage.py createsuperuser

# Create a .env file(See Below for more details.)

# Start Server
$ python manage.py runserver 0.0.0.0:80
# Head over to http://127.0.0.1/ to see the website.

# Head over to http://127.0.0.1/admin to add the voterlists in 'Voter lists' table and the candidates in the 'Candidates' table.

# Set the Voting Time in 'Vote auths' table(Create only one object and add the start and end time of voting).

# Now the project is ready for Voting!
```

# Environment Variables

1. Go to [API NINJA](https://api-ninjas.com/) and signup to obtain the api key for passphrase generation.
2. Create an Account on [TWILIO](https://www.twilio.com/try-twilio) and Buy a Phone Number to use the OTP Service.

Fill the .env file with the obtained values.

```
[+] Create a .env file in the root directory for the api tokens
    [-] API_NINJA_API = ''
    [-] TWILIO_ACCOUNT_SID = ''
    [-] TWILIO_AUTH_TOKEN = ''
    [-] TWILIO_PHONE_NUMBER = ''
```


## An Example Of ".env" File
```
API_NINJA_API = '/ghjf53spoG657vghjygdr0qw==uRVWERV'
TWILIO_ACCOUNT_SID = 'AA3w5fgdrfawd3459faedw4349a3b'
TWILIO_AUTH_TOKEN = 'awd18f3ccac7329thfsf43fd4drgx1'
TWILIO_PHONE_NUMBER = '+134656544'
```

