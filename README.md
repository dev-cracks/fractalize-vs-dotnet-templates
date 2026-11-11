# fractalize-vs-dotnet-templates

[![CI](https://github.com/dev-cracks/fractalize-vs-dotnet-templates/actions/workflows/ci.yml/badge.svg)](https://github.com/dev-cracks/fractalize-vs-dotnet-templates/actions/workflows/ci.yml)
[![CodeQL](https://github.com/dev-cracks/fractalize-vs-dotnet-templates/actions/workflows/codeql.yml/badge.svg)](https://github.com/dev-cracks/fractalize-vs-dotnet-templates/actions/workflows/codeql.yml)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/dev-cracks/fractalize-vs-dotnet-templates/badge)](https://scorecard.dev/viewer/?uri=github.com/dev-cracks/fractalize-vs-dotnet-templates)
[![Publish to Marketplace](https://github.com/dev-cracks/fractalize-vs-dotnet-templates/actions/workflows/publish-marketplace-vsix.yml/badge.svg)](https://github.com/dev-cracks/fractalize-vs-dotnet-templates/actions/workflows/publish-marketplace-vsix.yml)
[![Visual Studio 2022](https://img.shields.io/badge/Visual%20Studio-2022-5C2D91.svg?logo=visualstudio&logoColor=white)](https://visualstudio.microsoft.com/)
[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg)](LICENSE)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-fe5196.svg?logo=conventionalcommits&logoColor=white)](https://www.conventionalcommits.org/en/v1.0.0/)

> **Visual Studio item templates for Fractalize projects**: start every C# file with the conventions of the
> [engineering standards](docs/engineering-standards.md) already applied.

## 📦 Templates

| Template | What you get |
| --- | --- |
| Clean class with file-scoped namespace | A public class in a file-scoped namespace with an XML summary |

Install the extension from the Visual Studio Marketplace, then use **Add → New Item** and pick the
Fractalize template.

## 🔧 Building

The extension is a VSIX project and builds on Windows with Visual Studio 2022 (or MSBuild 17) and the
Visual Studio SDK:

```powershell
msbuild src/DevCracks.Fractalize.Templates.Vsix/DevCracks.Fractalize.Templates.Vsix.csproj /p:Configuration=Release /p:DeployExtension=false
```

Every push to `main` that changes `src/` builds the VSIX and publishes it to the Marketplace
([`publish-marketplace-vsix.yml`](.github/workflows/publish-marketplace-vsix.yml)).

## 🤝 Contributing

Read [`CONTRIBUTING.md`](CONTRIBUTING.md) before opening a pull request, and report vulnerabilities
privately as described in [`SECURITY.md`](SECURITY.md).

## 📄 License

[GPL-3.0](LICENSE) © Dev Cracks
