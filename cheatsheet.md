# Cheatsheet Übungsprojekt

## Inhaltsverzeichnis

+ [(Windows Subsystem für Linux) wsl commands](#windows-subsystem-für-linux-wsl-commands)
+ [Befehle in der Distro / Linux in PowerShell](#befehle-in-der-distro--linux-in-powershell)
+ [Neustart einer PowerShell/Terminal und Sprung in die DDEV Distro (s.o.) oder Start des DDEV(Ubuntu)-Terminal (Programme)](#neustart-einer-powershellterminal-und-sprung-in-die-ddev-distro-so-oder-start-des-ddevubuntu-terminal-programme)
+ [Git Installation in DDEV](#git-installation-in-ddev)
+ [Git SSH mit Linux](#git-ssh-mit-linux)
+ [Git mit GitHub verbinden !via SSH! – so wie es von GitHub vorgeschlagen wird](#git-mit-github-verbinden-via-ssh--so-wie-es-von-github-vorgeschlagen-wird)
+ [Weitere Git-Befehle](#weitere-git-befehle)
+ [daily Git-Befehle](#daily-git-befehle)
+ [.gitignore](#gitignore)
+ [nützliche Links](#nützliche-links)


### (Windows Subsystem für Linux) wsl commands
[*back to top*](#cheatsheet-übungsprojekt)

<table width="100%" cellpadding="2" cellspacing="0">
	<col width="128*"/>
	<col width="128*"/>
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl --update</font></p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.05cm"><p>
			Update für WSL</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl --install</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			installiert wsl + Standard Ubuntu und startet es</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl -l --all</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			listet alle installierten Linux-Distros auf</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl -l --running</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			listet nur die Distros auf, die aktuell laufen</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl -l -v (wsl –list --verbose)</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			listet alle Distros, deren Status und WSL-Version in welcher sie
			installiert sind</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl --shutdown</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			beendet alle Distros und WSL</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl --terminate Ubuntu</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			beendet die bezeichnete Distro (Ubuntu)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl --unregister Ubuntu</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			entfernt die Distro aus WSL mit allem was drin ist</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl --install Ubuntu --name DDEV</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			installiert ein Ubuntu unter dem name DDEV</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">wsl -d DDEV</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			startet die Distro DDEV / bzw. springt hinein</p>
		</td>
	</tr>
</table>

### Befehle in der Distro / Linux in PowerShell
[*back to top*](#cheatsheet-übungsprojekt)

<table width="100%" cellpadding="2" cellspacing="0">
	<col width="128*"/>
	<col width="128*"/>
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ exit</font></p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.05cm"><p>
			verlassen der Distro – zurück in PowerShell (die Distro läuft
			aber weiter)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ ddev --version</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			checkt welche Version von DDEV installiert ist (Installation siehe
			Links)</p>
		</td>
	</tr>
</table>

#### Neustart einer PowerShell/Terminal und Sprung in die DDEV Distro (s.o.) oder Start des DDEV(Ubuntu)-Terminal (Programme)
[*back to top*](#cheatsheet-übungsprojekt)

<table width="100%" cellpadding="2" cellspacing="0">
	<col width="128*"/>
	<col width="128*"/>
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">S ddev version</font></p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.05cm"><p>
			ist noch ausführlicher</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ docker ps</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			läuft docker?</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ cd ~</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			wechselt nach <i>home</i><span style="font-variant: normal"><span style="font-style: normal">/mylinux25/
			also in den Benutzer-Ordner des aktuellen Benutzers – dort
			gehören alle eigenen Dateien rein</span></span></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ cd
			kroepelinprojekt/Kursverwaltung</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			von Home weiter in den Projektordner</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ ddev config --auto</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			macht diesen Ordner zu einem ddev-Projektordner (.ddev wird
			eingefügt)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">ddev describe</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			zeigt infos zum projekt an</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ ddev start</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			startet das Projekt erstmals / jedesmal (es werden diverse Dateien
			downgeloadet)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ ddev launch</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			öffnet das Projekt im browser (man sieht da aber nix)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ ddev stop</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			stoppt das Projekt wieder</p>
		</td>
	</tr>
</table>

### Git Installation in DDEV
[*back to top*](#cheatsheet-übungsprojekt)

<table width="100%" cellpadding="2" cellspacing="0">
	<col width="128*"/>
	<col width="128*"/>
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ sudo apt-get install git</font></p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.05cm"><p>
			Installation unter Debian/Ubuntu</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git config --global user.name
			&quot;nusuth2025&quot;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			Einrichten des Users – der auch im Remote gilt</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">git config --global user.email
			&quot;211944562+nusuth2025@users.noreply.github.com&quot;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			Einrichten der e-mail – hier die anonyme e-mail aus dem
			GitHub-Konto</p>
		</td>
	</tr>
</table>

### Git SSH mit Linux
[*back to top*](#cheatsheet-übungsprojekt)

<table width="100%" cellpadding="2" cellspacing="0">
	<col width="128*"/>
	<col width="128*"/>
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ ls -al ~/.ssh</font></p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.05cm"><p>
			listet ssh Dateien im .ssh Ordner falls sie existieren</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.2cm">
			<font face="Consolas, monospace">$ ssh-keygen -t ed25519 -C
			&quot;email@ git.account&quot;</font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace">Antwort:</font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace">Your
			identification has been saved in /home/.../.ssh/id_ed25519</font></p>
			<p><font face="Consolas, monospace">Your public key has been saved
			in /home/.../.ssh/id_ed25519.pub</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			generiert ein neues SSH Key Paar 
			</p>
			<p style="margin-bottom: 0.2cm">ed25519 – ist ein
			Kryptographie-Verfahren</p>
			<p>– die Antwort gibt eine entsprechende Meldung mit Pfad und
			Fingerprint des Key (hier nicht zu sehen)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">eval &quot;$(ssh-agent -s)&quot;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			startet den SSH-Agent im Hintergrund</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ ssh-add ~/.ssh/id_ed25519</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			fügt den private Key dem SSH-Agent hinzu</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ cat ~/.ssh/id_ed25519.pub</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			gibt den angelegten Public Key aus</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.2cm">
			<font face="Consolas, monospace">den Public Key legt man in GitHub
			an</font></p>
			<p><font face="Consolas, monospace">https://github.com/settings/keys</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			den Public Key legt man in GitHub an</p>
			<p style="margin-bottom: 0.2cm">über Avatar&gt;Settings&gt;SSH
			and GPG Keys</p>
			<p>so kann man auch weiteren Benutzern Zugang gewähren, indem man
			ihre public SSH keys im Repository hinterlegt</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ ssh -T git@github.com</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			testet die Verbindung...</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ ddev auth ssh</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			fügt die SSH-Keys auch DDEV-SSH-Agenten hinzu?? (ob das nötig
			war??)</p>
		</td>
	</tr>
</table>

### Git mit GitHub verbinden !via SSH! – so wie es von GitHub vorgeschlagen wird 
(Https funktioniert nicht in DDEV – vermutlich weil kein Browser da ist?)
[*back to top*](#cheatsheet-übungsprojekt)

<table width="100%" cellpadding="2" cellspacing="0">
	<col width="128*"/>
	<col width="128*"/>
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ echo &quot;# Kursverwaltung&quot;
			&gt;&gt; README.md</font></p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.05cm"><p>
			<i>(optional) legt eine Readme.md an und schreibt die Überschrift
			in Markdown-Syntax in die Datei</i></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git init</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			macht das aktuelle Verzeichnis zu einem Git-Repository – zu
			erkennen am .git-Ordner</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git add README.md</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			<i>(optional) staged die Readme.md</i></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git commit -m &quot;first
			commit&quot;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			committed die Readme.md … oder was sonst so passiert ist</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch -M main</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			benennt den Branch um, vom ungeliebten Master zu main (Git macht
			wohl ursprünglich immernoch Master)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git remote add origin
			git@github.com:nusuth2025/Kursverwaltung.git</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			stellt die Verbindung zu GitHub als Origin her – wichtig: das
			funktioniert mit SSH – was vorher eingerichtet sein muss, denke
			ich</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git push <b>-u</b> origin main</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.5cm">
			<b>erster</b> push nach GitHub nach origin von main</p>
			<p>setzt gleichzeitig den upstream</p>
		</td>
	</tr>
</table>

### Weitere Git-Befehle
[*back to top*](#cheatsheet-übungsprojekt)

<table width="100%" cellpadding="2" cellspacing="0">
	<col width="128*"/>
	<col width="128*"/>
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.2cm">
			<font face="Consolas, monospace">$ git clone
			https://github.com/nusuth2025/Kursverwaltung.git</font></p>
			<p><font face="Consolas, monospace">$ git
			clonegit@github.com:nusuth2025/Kursverwaltung.git</font></p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.05cm"><p style="margin-bottom: 0.2cm">
			via Https: klont ein Repository von Remote nach lokal (also das
			Repository in dem der Befehl aufgerufen wird)</p>
			<p>oder via SSH-Verbindung, wenn sie eingerichtet ist (Keys in
			GitHub vorhanden) + Passphrase</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch main_br1</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			erzeugt einen neuen Branch (von dem Branch in dem man sich
			befindet, zu diesem Commitpunkt)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.2cm">
			<font face="Consolas, monospace">$ git checkout main_br1</font></p>
			<p><font face="Consolas, monospace">$ git switch main_br1</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			wechselt in den benannten Branch (der HEAD zeigt jetzt auf diesen
			Branch, der bei Start dem Commitpunkt des main entspricht)</p>
			<p><i>Vor dem Wechsel ggf. den Bearbeitungsstand der aktuellen
			Branch commiten!</i></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.2cm">
			<font face="Consolas, monospace">$ git checkout -b main_br1</font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace">$
			git switch -c main_br1</font></p>
			<p><font face="Consolas, monospace">$ git switch --create main_br1</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			erzeugt einen neuen Branch und wechselt direkt dorthin</p>
			<p><i>Vor dem Wechsel ggf. den Bearbeitungsstand der aktuellen
			Branch commiten!</i></p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git push <b>-u</b> origin
			main_br1</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			<b>erster</b> push nach GitHub nach origin von main_br1 (legt den
			Branch auch dort an)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.2cm">
			<font face="Consolas, monospace">$ git checkout main</font></p>
			<p><font face="Consolas, monospace">$ git merge main_br1</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			um zu Mergen – Wechsel in den Branch in den gemerged wird</p>
			<p>merged main_br1 in den aktuellen Branch main</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch -d main_br1</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			löscht den nicht mehr benötigten Branch main_br1</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.2cm">
			<font face="Consolas, monospace">Merge-Konflikte werden angezeigt
			durch die Datei in der der Konflikt besteht</font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace">und
			in der Datei durch:</font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace">&lt;&lt;&lt;&lt;&lt;&lt;&lt;
			HEAD: &lt;dateiname&gt;</font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace">Version
			in main</font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace">=========</font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace">Version
			in main_br1</font></p>
			<p><font face="Consolas, monospace">&gt;&gt;&gt;&gt;&gt;&gt;&gt;
			main_br1: &lt;dateiname&gt;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			zur Lösung des Konfliktes öffnet man die Datei (in main?) –
			löscht die Markierungen und Hinweise</p>
			<p style="margin-bottom: 0.2cm">&lt;&lt;&lt;&lt;&lt;&lt;&lt;
			====== &gt;&gt;&gt;&gt;&gt;&gt;&gt;</p>
			<p style="margin-bottom: 0.2cm">und lässt nur das drin, was die
			endgültige Version sein soll</p>
			<p>Danach erneut git add (und commit?)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			zeigt alle Branches – *Sternchen verweist auf den aktiven Branch</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch -v</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			wie oben nur mit Anzeige des letzten commit</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch -vv</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			wie oben mit Anzeige der Tracks/Verbindungen nach Remote</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch --merged</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			zeigt branches die in den aktiven gemerged wurden (und deswegen
			gelöscht werden könnten)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch --no-merged</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			zeigt die noch nicht in den aktuellen branch gemergeden branches</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch –move &lt;alter
			name&gt; &lt;neuer name&gt;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			ändert den Name eines Branch lokal</p>
			<p>(mitten im Projektverlauf nicht zu empfehlen)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git push –u origin &lt;neuer
			name&gt;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			bringt den neuen Namen auch nach Remote, als neuen Branch der eine
			Kopie des alten ist ??</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git push origin –delete
			&lt;alter name&gt;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			löscht den alten Name/Branch auch im Remote</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git branch --all</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			zeigt alle Branches remote und lokal</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git remote</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			zeigt die Remote Branches</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git remote -v</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			zeigt die Remotes etwas ausführlicher</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git checkout -b &lt;neuer
			branch&gt; [&lt;start-point&gt;]</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			erstellt einen neuen Branch und springt hinein</p>
			<p>start-point = Branch von dem er abgehen soll Bsp.:
			origin/main_b1 oder main_b1, default ist der aktuelle Branch</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.2cm">
			<font face="Consolas, monospace">$ git checkout -B &lt;(neuer)
			branch&gt; [&lt;start-point&gt;]</font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace"><i>------
			entspricht :</i></font></p>
			<p style="margin-bottom: 0.2cm"><font face="Consolas, monospace">$
			git branch -f &lt;(neuer) branch&gt; &lt;[start-point]&gt;</font></p>
			<p><font face="Consolas, monospace">$git checkout &lt;(neuer)
			branch&gt;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			erstellt einen neuen Branch falls er noch nicht existiert</p>
			<p>existiert er, wird er resetet auf den aktuellen Branch oder
			ggf. start-point und dahin gewechselt</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git push origin &lt;(neuer)
			branch&gt;</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			pusht den neuen Branch nach GitHub (-u ist nicht sinnvoll)</p>
		</td>
	</tr>
</table>

### daily Git-Befehle
[*back to top*](#cheatsheet-übungsprojekt)

<table width="100%" cellpadding="2" cellspacing="0">
	<col width="128*"/>
	<col width="128*"/>
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git status</font></p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.05cm"><p>
			zeigt aktuellen Status</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.2cm">
			<font face="Consolas, monospace">$ git add &lt;dateiname&gt;
			&lt;dateiname&gt;</font></p>
			<p><font face="Consolas, monospace">$ git add --all</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			staged einzelne Dateien</p>
			<p>oder alles was untracked ist (und nicht im .gitignore steht)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git commit -a -m “message“</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			commited alles, was gestaged ist, mit Message</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git push origin main</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			pusht von local/main auf origin/main (also auf remote)</p>
			<p>wenn origin/main nicht existiert, wird es erstellt</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git push origin
			main:otherbranch</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			pusht von local/main auf origin/otherbranch</p>
			<p>– ungetestet – 
			</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git push origin :otherbranch</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.2cm">
			Achtung!!!! das löscht origin/otherbranch</p>
			<p>– ungetestet – 
			</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">$ git pull origin main</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			holt den aktuellen Stand von Remote (origin) Branch (main) in das
			aktuelle Repository</p>
		</td>
	</tr>
</table>

### .gitignore
[*back to top*](#cheatsheet-übungsprojekt)

<table width="100%" cellpadding="2" cellspacing="0">
	<col width="128*"/>
	<col width="128*"/>
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<a href="https://www.w3schools.com/git/git_ignore.asp"><font face="Consolas, monospace">https://www.w3schools.com/git/git_ignore.asp</font></a></p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.05cm"><p>
			für weitere Infos (fürs Testen reicht git status)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="font-style: normal; font-variant: normal">
			<font face="Consolas, monospace">/name/</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			ignoriert alle Ordner <i>name</i> in root (also da wo der
			.git-Ordner auch liegt)</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">/name</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			ignoriert alle Ordner und Dateien (Endung egal) <i>name</i> in
			root 
			</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">**/name</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			ignoriert jeden Ordner <i>name</i> auch in Unterordnern</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">name</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			ignoriert Ordner (mit Inhalt) und Dateien (Endung egal) die <i>name</i>
			heißen egal wo sie liegen</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p>
			<font face="Consolas, monospace">name.file</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			ignoriert genau diese Datei egal wo</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.5cm">
			<font face="Consolas, monospace">*name</font></p>
			<p><font face="Consolas, monospace">name*</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p style="margin-bottom: 0.5cm">
			ignoriert alle Ordner und Dateien deren Name mit <i>name</i> endet</p>
			<p>… mit <i>name</i> anfängt</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><p style="margin-bottom: 0.5cm">
			<font face="Consolas, monospace">*.file</font></p>
			<p><font face="Consolas, monospace">!name.file</font></p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0.05cm"><p>
			ignoriert jede .<i>file</i>-Datei überall außer <i>name.file</i></p>
		</td>
	</tr>
</table>

### nützliche Links
[*back to top*](#cheatsheet-übungsprojekt)

* https://ddev.com/get-started/
* https://ddev.com/blog/watch-new-windows-installer/
* https://docs.github.com/en/authentication
* https://code.visualstudio.com/docs/sourcecontrol/overview
* https://git-scm.com/book/de/v2/Git-Branching-Branching-Workflows

[*back to top*](#cheatsheet-übungsprojekt)