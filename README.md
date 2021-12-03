<!-- Badge for License -->
<div align="right">

  [![](https://img.shields.io/github/license/Hsins/yogurt.svg?style=flat-square)](./LICENSE)

</div>

<!-- Logo, Title and Description -->
<div align="center">

  <img src="https://i.imgur.com/lTGFDQx.png" alt="yogurt" height="150px">

# Yogurt

🍨 _A sweet [Scoop](https://github.com/ScoopInstaller/Scoop) bucket containing JSON [app manifests](https://scoop-docs.vercel.app/docs/concepts/App-Manifests.html) which describe how to install an application._

</div>

## Usage

Make sure that you've installed the Windows Package Manager [Scoop](https://github.com/ScoopInstaller/Scoop) on your machine.

```powershell
# enable remote policy in PowerShell
> Set-ExecutionPolicy RemoteSigned -scope CurrentUser

# customize the Scoop directory (e.g. 'C:\ProgramData\scoop')
> $env:SCOOP='C:\ProgramData\scoop'
> [Environment]::SetEnvironmentVariable('SCOOP', $env:SCOOP, 'User')

# install Scoop (use one of commands shown below)
> Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
> iwr -useb get.scoop.sh | iex
```

Add this bucket for installing extra applications.

```powershell
# add bucket and update scoop
> scoop bucket add yogurt https://github.com/Hsins/yogurt
> scoop update

# install applications
> scoop install yogurt/<APPLICATION>
```

## Applications

- [`drawio`](./bucket/drawio.json): A diagramming and whiteboarding desktop app based on Electron that wraps the core draw.io editor.
- [`irontcl`](./bucket/irontcl.json): A binary distribution of Tcl and Tk by Eyrie Solutions. Providing signed binaries for Windows, based on the latest official release.
- [`komodoide`](./bucket/KomodoIDE.json): An universal IDE provides more robust functionality such as debugging, unit testing, code refactoring and code profiling.
- [`magicsplat-tcl`](./bucket/magicsplat-tcl.json): The Magicsplat Tcl/Tk for Windows distribution. A binary Windows Installer based distribution of Tcl/Tk for Windows systems. It includes commonly used libraries, extensions and development tools.

## References

- [Ash258/GenericBucket](https://github.com/Ash258/GenericBucket)
- [Ash258/Shovel-Ash258](https://github.com/Ash258/Shovel-Ash258)
- [App Manifests | Scoop Documentation](https://scoop-docs.vercel.app/docs/concepts/App-Manifests.html)

## License

Licensed under the MIT License, Copyright © 2020-present Hsins.