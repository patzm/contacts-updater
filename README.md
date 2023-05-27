# contacts-updater :card_index: :arrows_counterclockwise:
Updates contacts in the *Contacts* app on macOS.
Specifically, the following features are supported:
* Download a new profile picture if a contact doesn't have one yet.
* If social media providers are used, stores the profile information in the contact.

Sources / providers:
* [Gravatar](https://gravatar.com)
* [LinkedIn](https://www.linkedin.com/) by crawling with [Selenium](https://selenium-python.readthedocs.io/index.html)

By default, all providers are enabled.
Each one can be disabled using the `providers` sub-parser.
Just invoke `--help` to see how to use it.

## Disclaimer :warning:
Use this tool at your own risk.

* Using this tool may violate the terms of service (TOS) of some providers / platforms.
* Storing the password in clear text is a risk.
  If someone has access to your machine, the password may be at risk.

## Setup
Clone the repository
```shell
git clone https://github.com/patzm/contacts-updater.git
cd contacts-updater
```

Install the requirements
```shell
brew install geckodriver

# maybe from within a virtual environment
pip install -r requirements.txt
```

Prepare the executable
```shell
chmod +x update-contacts
````

## Running it
If this is the first time you are running the script, and if you want to use all providers, credentials must be provided.
Run this once and then fill in the values
```shell
./update-contacts --gen-config-files
```

Run the contact picture updater
```shell
./update-contacts
```