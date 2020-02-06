# Preparational Steps

Package Manager unter Windows? JA!

##### Chocolatey:  <https://chocolatey.org/>

---

#### Chocolatey - Installation mit powershell

Siehe auch: <https://chocolatey.org/install>

1. powershell im admin Modus öffnen:
   1. Windows Suche -> Powershell -> Rechtsklick und Start als Admin
2. Eingabe des folgenden Befehls:

```bash
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

3. powershell schließen und wieder im Admin Modus öffnen

---

#### docker-toolbox - Installation

In Powershell (admin) folgenden Befehl eingeben

```bash
# NUR falls virtualbox noch nicht installiert
choco install virtualbox -y

# "must have"
choco install docker-toolbox -y

# another "must-have"
choco install vscode -y

# [optional] git Versionsverwaltung (git bash und ssh funktioniert dann sicher)
choco install git -y
```

> Thats it!

---

#### Linux Users (untested!)

Nur docker-machine:

```bash
$ base=https://github.com/docker/machine/releases/download/v0.16.0 &&
  curl -L $base/docker-machine-$(uname -s)-$(uname -m) >/tmp/docker-machine &&
  sudo install /tmp/docker-machine /usr/local/bin/docker-machine
```

oder "full docker" z.B. debian: <https://docs.docker.com/install/linux/docker-ce/debian/>

---

#### Ein paar chocolatey Befehle

```bash
# installation eines packages - []..optional
choco install <package-name> [-y]

# liste lokal installierter programme
choco list -lo

# liste aller programme, die mit docker zu tun haben 
choco list docker

# deinstallation
choco uninstall <package> -y

# update all
choco upgrade all -y

# update einzelens package
choco upgrade <package> -y
```

---

### Optionale Installationen

1. Markdown-Reader (Dokumente im md-Format): `choco install typora -y`
2. *TIPP*: Virtualisierungs Skripting für Development: `choco install vagrant -y` 

---

### Deinstallationsschritte nach dem Seminar

```bash
choco uninstall <package> -y
```

Und dann möchte ich auf <https://chocolatey.org/docs/uninstallation> verweisen.
