## Django API Deployment

### [Django Settings](https://djangostars.com/blog/configuring-django-settings-best-practices/)

- Differnent Environments
  - examples:
    - local, dev, ci, `DEBUG = True`, verbose logging, additional apps

- Sensitive Data
  - `SECRET_KEY`
  - db passwords
  - api tokens

#### Options
- Creating a `settings_local.py`
  - have a separate local environment 
- Create separate settings file for each environment
  - a full settings folder
- Create a environment variables page
  - `os.environ` is the base page
  - do have to handle KeyError exceptions

#### 12 Factors
  - recommendations to build distributed web-apps
- Codebase
- Dependecies
- Config
- Backing Servieces
- Build, realease, run
- Processes
- Port Binding
- Concurrency
- Diposability
- Dev/prod parity
- Logs
- Admin Process
- [The recommendations at 12factor.net](https://12factor.net/)

- `.env`
  - place all environment variables 
  - ex. : `database_url`, `secret_key`, `debug`

### [SSH Tutorial](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work)
- SSH
  - secrue Shell
- ability to access a remote server over the Internet
- cryptographic techniques protect inormation flow
- Encryptions
  - symmetrical
  - asymmetrica
  - hashing
    - not to be decrypted but to allow for verification

[Return to Home](README.md)