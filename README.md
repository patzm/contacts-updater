# contacts-updater
Updates contact pictures on macOS.

Sources:
- [Gravatar](https://gravatar.com)
- [LinkedIn](https://www.linkedin.com/) by crawling with [Selenium](https://selenium-python.readthedocs.io/index.html)

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