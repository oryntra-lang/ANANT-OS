# ANANT OS

**Your AI-powered personal computing environment.**

ANANT OS is a Linux-based personal computing environment with a natural-language AI assistant at its core. The goal is to let people interact with their computer through voice and text while keeping the user in control of important actions.

> **Project status:** Initial setup. The BlueBuild template has been generated; ANANT-specific customization and implementation are in progress. Features described below are goals unless explicitly marked as implemented.

## Vision

ANANT should be more than a chatbot. It should become a capable personal computer operator that can understand a request, plan the steps, use approved tools, verify what happened, and clearly report the result.

## Project goals

- **Natural interaction:** Hindi and English voice and text commands.
- **Computer assistance:** Help with applications, files, settings, and browser workflows.
- **Task automation:** Execute multi-step workflows with clear progress and verified results.
- **System dashboard:** Show useful device information such as CPU, memory, storage, and network status.
- **Privacy and security:** Protect credentials and request confirmation for sensitive actions.
- **Reliability:** Provide logs, error handling, recovery paths, and safe updates.
- **User control:** Make permissions understandable, scoped, and revocable.

## Planned capabilities

| Component | Planned responsibility |
|---|---|
| ANANT AI Core | Understand requests, plan tasks, and communicate in Hindi and English |
| Voice interface | Speech input and spoken responses |
| Computer operator | Approved interaction with desktop applications and browser |
| File assistant | Search, organize, and manage files with confirmation for destructive actions |
| Automation engine | Run multi-step tasks and report verified outcomes |
| System monitor | Display hardware and system health |
| Security layer | Protect secrets, scope permissions, and pause for OTP/CAPTCHA or user-only checks |
| Update and recovery | Support tested updates and documented rollback/recovery |

These are project goals, not claims that the features are already implemented.

## OS foundation

This repository uses [BlueBuild](https://blue-build.org/) to build a custom image based on an immutable Fedora Atomic desktop. The base image, desktop environment, package set, and build pipeline will be documented as they are selected and tested.

BlueBuild is the image-building foundation. The ANANT assistant and its services are separate components that will be developed on top of the operating system.

## Design principles

1. **Human in control:** Never silently perform high-impact or irreversible actions.
2. **Verify before reporting:** Distinguish a requested action from an action that actually succeeded.
3. **Least privilege:** Use only the permissions needed for a task.
4. **Secure by default:** Never expose passwords, API keys, or session tokens in logs or speech.
5. **Transparent operation:** Explain what the assistant is doing and provide useful error details.
6. **Recoverability:** Prefer reversible changes and document recovery procedures.

## Development roadmap

- [ ] Confirm target hardware and supported architecture.
- [ ] Select the Fedora Atomic base image and desktop environment.
- [ ] Review and customize the BlueBuild image recipe.
- [ ] Build and test a bootable image.
- [ ] Define the ANANT AI Core service architecture.
- [ ] Add desktop integration and voice interaction.
- [ ] Implement permission-aware computer automation.
- [ ] Add system monitoring, update, and recovery workflows.
- [ ] Publish installation and contribution documentation.

Roadmap items will be checked off only after they are implemented and tested.

## Repository layout

The BlueBuild template files are the starting point. The structure will evolve with implementation. Planned areas include:

- `recipes/` — BlueBuild image recipes.
- `files/` — Files and configuration included in the image.
- `modules/` — Reusable image build modules.
- `anant-core/` — AI assistant services (planned).
- `desktop/` — Desktop integration and interface (planned).
- `docs/` — Architecture, setup, security, and development guides.

## Getting started

1. Review the [BlueBuild setup documentation](https://blue-build.org/how-to/setup/).
2. Inspect the existing recipe and workflow files before changing the image.
3. Build and test the image in a virtual machine before installing it on physical hardware.
4. Follow the installation instructions generated for the actual image and release. Do not rebase a daily-use machine until the image has been built, verified, and tested.

Build and installation instructions will be expanded as the project configuration is finalized.

## Contributing

The project is at an early stage. Issues and discussions about architecture, hardware support, accessibility, security, and user experience are welcome. Please do not submit secrets, credentials, personal data, or private system logs.

Contribution instructions and development setup will be added once the initial build pipeline is in place.

## Security

Never commit passwords, API keys, access tokens, private keys, or personal information. Security-sensitive reports should not be posted publicly with exploitable details; use GitHub's private vulnerability reporting if it is enabled for this repository.

## License

A license has not yet been selected. Until a license file is added, no additional permissions should be assumed for reuse, modification, or distribution.
