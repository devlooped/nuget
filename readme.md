NuGet Contribution Graph
===

Generates and updates the nuget.json file containing all active nuget packages, their associated repositories and contributors.

> An active nuget package has at least 200 downloads per day in aggregate across the last 5 versions.

The static [nuget.json](nuget.json) file (updated once a month via a [workflow](.github/workflows/nuget.yml)) can be used in shields.io badges.
The following are generated from the latest version, entirely server-less:

![NuGet Packages](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2Fnuget.json&query=%24.summary.packages&style=social&logo=nuget&label=packages)
![Daily Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2Fnuget.json&query=%24.summary.downloads&style=social&logo=nuget&label=daily%20downloads
)

Source:

```
![NuGet Packages](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2Fnuget.json&query=%24.summary.packages&style=social&logo=nuget&label=packages)

![Daily Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2Fnuget.json&query=%24.summary.downloads&style=social&logo=nuget&label=daily%20downloads
)
```

Additional package owners can be added via [owners.json](owners.json) so that all package stats can be collected for 
the given accounts. Static badges can then be used for those, such as: 

[![NuGet Packages](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2FDevlooped.json&query=%24.summary.packages&style=social&logo=nuget&label=devlooped%20packages)](https://www.nuget.org/profiles/devlooped)
[![Daily Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2FDevlooped.json&query=%24.summary.downloads&style=social&logo=nuget&label=daily%20downloads
)](https://www.nuget.org/profiles/devlooped)

## SponsorLink Endpoint Badges

The [SponsorLink reference implementation](https://www.devlooped.com/SponsorLink/github/) complements this 
repo by providing support for the same shields.io badges for specific github accounts. 

Examples:

[![xunit dl/day](https://img.shields.io/endpoint?label=xunit%20downloads%2Fday&style=social&logo=nuget&url=https%3A%2F%2Fsponsorlink.devlooped.com%2Fnuget%2Fdl?owner=xunit)](https://www.nuget.org/profiles/xunit)
[![Popular NuGets](https://img.shields.io/endpoint?label=popular%20nugets&style=social&logo=nuget&url=https%3A%2F%2Fsponsorlink.devlooped.com%2Fnuget%2Fid?owner=xunit)](https://www.nuget.org/profiles/xunit)

[![Prism dl/day](https://img.shields.io/endpoint?label=Prism%20daily%20downloads&color=blue&logo=nuget&url=https%3A%2F%2Fsponsorlink.devlooped.com%2Fnuget%2Fdl%3Fowner%3DPrismLibrary)](https://www.nuget.org/profiles/PrismLibrary)
[![Popular NuGets](https://img.shields.io/endpoint?label=Prism%20favorites&style=social&logo=nuget&url=https%3A%2F%2Fsponsorlink.devlooped.com%2Fnuget%2Fdl%3Fowner%3DPrismLibrary)](https://www.nuget.org/profiles/PrismLibrary)

[![Devlooped Downloads](https://img.shields.io/endpoint?label=devlooped%20daily&logo=githubsponsors&color=ea4aaa&url=https%3A%2F%2Fsponsorlink.devlooped.com%2Fnuget%2Fdl%3Fowner%3Ddevlooped%26owner%3Dmoq)](https://www.nuget.org/profiles/devlooped)
[![Popular NuGets](https://img.shields.io/endpoint?label=loved%20nugets&style=social&logo=nuget&url=https%3A%2F%2Fsponsorlink.devlooped.com%2Fnuget%2Fid%3Fowner%3Ddevlooped%26owner%3Dmoq)](https://www.nuget.org/profiles/devlooped)

[![jbogard Downloads](https://img.shields.io/endpoint?url=https%3A%2F%2Fsponsorlink.devlooped.com%2Fnuget%2Fdl%3Fowner%3Djbogard)](https://www.nuget.org/profiles/AutoMapper)
[![AutoMapper NuGets](https://img.shields.io/endpoint?logo=nuget&url=https%3A%2F%2Fsponsorlink.devlooped.com%2Fnuget%2Fid%3Fowner%3DAutoMapper)](https://www.nuget.org/profiles/AutoMapper)

The `https://sponsorlink.devlooped.com/nuget/[all/dl]?[login]` Azure functions URL filters and sumarizes the [nuget.json](nuget.json) file for the given github login.
