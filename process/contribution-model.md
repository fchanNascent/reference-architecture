# Contribution Model

## Why

- As a tool Git combined with GitHub provides countless styles of development and project management with many options for configuration such as:
    - Trunk based development (w/feature flagging)
    - GitFlow (branches/features)
    - Pull Requests (core contributers / open source)

## What

This document provides a standard for practices around the contribution model for Telus Digital that should:

- Reduce the time required to onboard new developers
- Reduce friction for developers contributing to other projects
- Provide clarity on expectations for leads in how to model new projects, and coach their teams in contributing
    
## How

There has been a constant swing between Trunk Based Development and Branch style development for many years. Reasonably so, both are seen to have advantages and disadvantages. 
- Small branches with Pull Requests encourage a social open source model, a living form of documentation, and an easy way for external contributors to see and understand the contribution model
- Trunk Based development can assist in reducing defects and reduce day to day frictions for core team members. 

In this way teams are encouraged to adopt a hybrid approach:
- Each project should have core owners that oversee the vision of the project, and can reject/approve Pull Requests and are responsible for supporting and communicating with interested contributors.
- Teams should be comfortable using small branches with PRs, and should practice this as a way of creating transparency in the code base and encouraging external contributors to participate
- Trunk based development is acceptable, but more as a philosophical approach to reducing internal day to day frictions for the core team, not as a mandate
 
### Commit Template
 For standardized git commits projects should use Commitizen with conventional-changelog adapter 
 
 This can be setup by running the following in your projects root:
 
```
//Install commitizen globally if you have not already installed it
npm install commitizen -g 

//This initializes your actual project config by installing the adapter, and adding the config to your package.json
commitizen init cz-conventional-changelog --save-dev --save-exact
```

Once installed, git commits using the commitizen tool can be made with:
```
git cz -a
```

This can be hooked into your commit-msg git-hook to ensure all commit messages utilize this format.
 
 
## References
- [Open Source Guides][open-source-guides]
- [Trunk Based Development - History][trunk-based-development]
- [Commitizen][commitizen]

[open-source-guides]: https://opensource.guide/ "Open Source Guides"
[trunk-based-development]: https://trunkbaseddevelopment.com/game-changers/ "History of Trunk Based Development"
[commitizen]: https://github.com/commitizen/cz-cli#making-your-repo-commitizen-friendly
