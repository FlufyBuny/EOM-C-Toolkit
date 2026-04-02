## Changelog
See [CHANGELOG.md](./CHANGELOG.md) for version history.

## Project

EPSILON – Exchange Online & Compliance Toolkit

EPSILON is a PowerShell-based administrative toolkit designed to simplify and streamline common tasks in Microsoft 365, specifically across Exchange Online and the Compliance (Purview) Center.

Built with MSP workflows in mind, EPSILON provides a menu-driven interface for fast, repeatable operations without needing to remember complex PowerShell commands.

## Project Structure

This repository includes three deployment formats:

Windows PowerShell Script<br>
EOM - v1.1.ps1<br>
Full interactive menu for Exchange Online & Compliance tasks

macOS PowerShell Script<br>
EOM - v1.1 - MAC.ps1<br>
Compatible with PowerShell Core (pwsh) on macOS

Executable Version<br>
EOM - v1.1.exe<br>
Packaged version of the PowerShell script for simplified execution<br>
Note: This is a wrapped .ps1, not a compiled binary

## Features<p>
Exchange Online<br>
List mailboxes<br>
View mailbox details<br>
Create mailboxes<br>
Remove mailboxes<br>
Enable archive mailbox<br>
Enable auto-expanding archive<br>
Trigger Managed Folder Assistant<br>
View inbox rules<br>
Remove inbox rules<br>
Compliance (Purview)<br>
Create Compliance Searches (by subject)<br>
Start and monitor searches<br>
Purge emails from tenant<br>
Status tracking and completion loops<br>

## Requirements
PowerShell 5.1+ (Windows) or PowerShell Core (macOS/Linux)<br>

Microsoft modules:
ExchangeOnlineManagement<br>
Microsoft.Graph (optional depending on usage)

If modules are missing, EPSILON can prompt or install them automatically (depending on version).

Permissions Required

Exchange Admin or Global Admin<br>
Compliance Admin (for Purview features)<br>

## Usage
Windows (PS1)<br>
Set-ExecutionPolicy Bypass -Scope Process -Force .\EOM - v1.1.ps1

macOS (PowerShell Core)
pwsh ./EOM - v1.1 - MAC.ps1

Executable
EOM - v1.1.exe

Execution Policy / Security

If you encounter script blocking:

Set-ExecutionPolicy Bypass -Scope Process -Force

This allows the script to run without permanently lowering system security.

Notes
The EXE version is a wrapped PowerShell script and may still trigger security warnings.
Some features (like Compliance purge) can take time — EPSILON includes built-in progress loops.
Managed Folder Assistant errors (RPC issues) are typically server-side and not caused by the script.

## Known Issues

Start-ManagedFolderAssistant may return:

RPC Error -2147220992

This is a Microsoft service-side issue and usually resolves on retry.

Inbox rule creation timestamps are not directly exposed via standard cmdlets.

## Roadmap / Future Enhancements

CSV reporting/export options<br>
GUI version<br>
Enhanced rule auditing (creation metadata if available)<br>
Better error handling and retry logic<br>
Integration with Microsoft Graph for deeper insights<br>

## Contributing

Contributions, improvements, and ideas are welcome.

If you’re an MSP or admin using this in production, feel free to submit:

Feature requests
Bug reports<br>
Enhancements<br>
License

This project is provided as-is for administrative use.<br>
Customize freely for internal or client environments.

Developed for real-world MSP operations to reduce friction and increase efficiency in Microsoft 365 administration.

![Version](https://img.shields.io/badge/version-v1.1-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS-lightgrey)
![PowerShell](https://img.shields.io/badge/powershell-5.1%2B%20%7C%20Core-blue)
