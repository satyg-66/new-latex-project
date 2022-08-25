# New LaTeX project
Creates a new LaTeX project based on a predefined template stored on your system. *(template not included in this repository)* Also, the project will immediatly open in [Code](https://github.com/microsoft/vscode/) texteditor. 

## Dependencies
This project is made for **Manjaro** and therefor all dependencies needed are based on that. In case of using e.g., a Debian based system - dependencies may vary.

- [texlive-bin](https://archlinux.org/packages/extra/x86_64/texlive-bin/)
- [texlive-formatsextra](https://archlinux.org/packages/extra/any/texlive-formatsextra/)
- [texlive-latexextra](https://archlinux.org/packages/extra/any/texlive-latexextra/)
- [texlive-bibtexextra](https://archlinux.org/packages/extra/any/texlive-bibtexextra/)
- [LaTeX Workshop plugin](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

***NOTE***: *These dependencies may also vary depending on your predefined-template.*

Hence, that you need the previous mentioned editor installed on your system. This can be installed using below command for Arch based distributions, such as Manjaro.

```
sudo pacman -S code
```
or with below command if using a Debian based distribution.

```
sudo snap install codium --classic
```
***NOTE***: *Debian based distributions need to install [codium](https://vscodium.com/) as a snap package.*

---

## How to use the script
Before running the script it has to be made executable. Navigate to the directory containing the script and run the command:
```
chmod +x report
```

Best practice is to create an alias in your `.bashrc`, `config.fish`, or what ever shell you use. Below is an example on how it may look when using fish.

```
alias report='./script/python/LaTeX/report'
```

when calling the script you need to specify **new-project-name** and **path-to-new-project**. Below is an example on how to create a new project named *new-project* in the `~/Documents` directory - after using an alias.

```
report new-project ~/Documents
```

---
## Reminder

There is a friendly reminder built in to the code as can be seen below - to remind you in cases when calling the script without arguments.

```python
else:
        print('''You need to specify "project-name" and "path"
        example: latex new-project ~/Documents''')
```