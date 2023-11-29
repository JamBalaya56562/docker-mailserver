<h1 align="center">docker-mailserver</h1>

<p align="center">
  <a aria-label="docker" href="https://www.docker.com/">
    <img src="https://img.shields.io/badge/-docker-2496ED.svg?logo=docker&style=for-the-badge&labelColor=000000" alt="docker">
  </a>
  <a aria-label="dovecot" href="https://www.dovecot.org/">
    <img src="https://img.shields.io/badge/-dovecot-54BCAB.svg?logo=dovecot&style=for-the-badge&labelColor=000000" alt="dovecot">
  </a>
  <a aria-label="Let's Encrypt" href="https://letsencrypt.org/">
    <img src="https://img.shields.io/badge/-letsencrypt-003A70.svg?logo=letsencrypt&style=for-the-badge&labelColor=000000" alt="Let's Encrypt">
  </a>
  <a aria-label="License" href="https://github.com/JamBalaya56562/nginx-proxy/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/JamBalaya56562/nginx-proxy?style=for-the-badge&labelColor=000000" alt="License">
  </a>
</p>

<p align="center">
  A production-ready fullstack but simple containerized mail server📧
</p>

## ⚒️ Usage

### 1. Clone
To clone and run this application, you'll need [Git](https://git-scm.com) and [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed on your computer.  
From your command line:

```bash
# Clone this repository
$ git clone https://github.com/JamBalaya56562/docker-mailserver
```

### 2. Set variables in the `.env` file
`DOMAIN1` is **mail** server domain.  
`DOMAIN2` is **host** server domain.  
`NETWORK` is whatever you like.

```diff
# For example
- DOMAIN1=
- DOMAIN2=
- NETWORK=
+ DOMAIN1=mail.example.com
+ DOMAIN2=example.com
+ NETWORK=nginx_web
```
### 3. Docker Compose
```bash
# Check if variables are appropriate
$ docker compose convert

# Run and up the containers using docker compose
$ docker compose up -d

# Make sure if there are errors in the containers
$ docker compose logs
```

## 📑 Reference

[Docker Mailserver](https://docker-mailserver.github.io/docker-mailserver/latest/)

## 📦 Credits

This software uses the following packages:

- [Docker](https://www.docker.com/)
- [docker-mailserver](https://github.com/docker-mailserver/docker-mailserver)
- [Postfix](http://www.postfix.org) with SMTP or LDAP authentication and support for [extension delimiters](https://docker-mailserver.github.io/docker-mailserver/latest/config/user-management/aliases/#address-tags-extension-delimiters-an-alternative-to-aliases)
- [Dovecot](https://www.dovecot.org) with SASL, IMAP, POP3, LDAP, [basic Sieve support](https://docker-mailserver.github.io/docker-mailserver/latest/config/advanced/mail-sieve) and [quotas](https://docker-mailserver.github.io/docker-mailserver/latest/config/user-management/accounts#notes)
- [Rspamd](https://rspamd.com/)
- [Amavis](https://www.amavis.org/)
- [SpamAssassin](http://spamassassin.apache.org/) supporting custom rules
- [ClamAV](https://www.clamav.net/) with automatic updates
- [OpenDKIM](http://www.opendkim.org) & [OpenDMARC](https://github.com/trusteddomainproject/OpenDMARC)
- [Fail2ban](https://www.fail2ban.org/wiki/index.php/Main_Page)
- [Fetchmail](http://www.fetchmail.info/fetchmail-man.html)
- [Getmail6](https://getmail6.org/documentation.html)
- [Postscreen](http://www.postfix.org/POSTSCREEN_README.html)
- [Postgrey](https://postgrey.schweikert.ch/)
- Support for [LetsEncrypt](https://letsencrypt.org/), manual and self-signed certificates
- A [setup script](https://docker-mailserver.github.io/docker-mailserver/latest/config/setup.sh) for easy configuration and maintenance
- SASLauthd with LDAP authentication
  
## 📄 License

The MIT License Copyright (c) 2023 - [JamBalaya56562](https://github.com/JamBalaya56562).  
Please have a look at the [LICENSE](https://github.com/JamBalaya56562/docker-mailserver/blob/main/LICENSE) for more details.
