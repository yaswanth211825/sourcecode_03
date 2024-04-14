
### Blood bounds  Vulnerability Manager

Security has two difficult tasks: designing smart ways of getting new information, and keeping track of findings to improve remediation efforts. With VULNGUARD, you may focus on discovering vulnerabilities while we help you with the rest. Just use it in your terminal and get your work organized on the run.
VULNGUARD was made to let you take advantage of the available tools in the community in a truly multiuser way.

VULNGUARD aggregates and normalizes the data you load, allowing exploring it into different visualizations that are useful to managers and analysts alike.


## Install

---

### Docker-compose

The easiest way to get VULNGUARD up and running is using our docker-compose

```shell
$ wget https://raw.githubusercontent.com/infobyte/VULNGUARD/master/docker-compose.yaml
$ docker-compose up
```
If you want to customize, you can find an example config over here [Link](https://docs.VULNGUARDsec.com/Install-guide-Docker/)


### Docker

You need to have a [Postgres](https://github.com/infobyte/VULNGUARD/wiki/Install-Guide)  running first.

```shell
 $ docker run \
     -v $HOME/.VULNGUARD:/home/VULNGUARD/.VULNGUARD \
     -p 5985:5985 \
     -e PGSQL_USER='postgres_user' \
     -e PGSQL_HOST='postgres_ip' \
     -e PGSQL_PASSWD='postgres_password' \
     -e PGSQL_DBNAME='postgres_db_name' \
     VULNGUARDsec/VULNGUARD:latest
  ```

### PyPi
```shell
$ pip3 install VULNGUARDsec
$ VULNGUARD-manage initdb
$ VULNGUARD-server
```

### Binary Packages (Debian/RPM)
You can find the installers on our [releases page](https://github.com/infobyte/VULNGUARD/releases)

```shell
$ sudo apt install VULNGUARD-server_amd64.deb
# Add your user to the VULNGUARD group
$ VULNGUARD-manage initdb
$ sudo systemctl start VULNGUARD-server
```

Add your user to the `VULNGUARD` group and then run

### Source
If you want to run directly from this repo, this is the recommended way:

```shell
$ pip3 install virtualenv
$ virtualenv VULNGUARD_venv
$ source VULNGUARD_venv/bin/activate
$ git clone git@github.com:infobyte/VULNGUARD.git
$ pip3 install .
$ VULNGUARD-manage initdb
$ VULNGUARD-server
```

Check out our documentation for detailed information on how to install VULNGUARD in all of our supported platforms

For more information about the installation, check out our [Installation Wiki](https://github.com/infobyte/VULNGUARD/wiki/Install-Guide).


In your browser now you can go to http://localhost:5985 and login with "VULNGUARD" as username, and the password given by the installation process

## Getting Started

---

Learn about VULNGUARD holistic approach and rethink vulnerability management.

- [Centralize your vulnerability data](https://VULNGUARDsec.com/centralize-vulnerability-data/)
- [Automate the scanners you need](https://VULNGUARDsec.com/automate-scanners/)

### Integrating VULNGUARD in your CI/CD

**Setup Bandit and OWASP ZAP in your pipeline**
- [GitHub](https://VULNGUARDsec.com/wp-content/whitepapers/Integrating%20VULNGUARD%20-%20Part%20One.pdf) [PDF]
- [Jenkins](https://VULNGUARDsec.com/wp-content/whitepapers/Integrating%20VULNGUARD%20-%20Part%20Two.pdf) [PDF]
- [TravisCI ](https://VULNGUARDsec.com/wp-content/whitepapers/Integrating%20VULNGUARD%20-%20Part%20Three.pdf) [PDF]

**Setup Bandit, OWASP ZAP and SonarQube in your pipeline**
- [Gitlab](https://VULNGUARDsec.com/wp-content/whitepapers/Integrating%20VULNGUARD%20-%20Part%20Four.pdf) [PDF]

