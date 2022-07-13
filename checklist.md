# Planning
## What do I want to accomplish?
Set up a fresh install of any of my machines to have my everyday tools and configurations.

## How can you complete your goal?
Since I would like to use this to setup Linux, Windows and Mac OS systems, I think that 
shell scripting may not be truly cross-platform in my use case.  
A standalone tool may require more time to setup, as well. Could be used to learn something
new, though.

## Requirements:
- I don't care much about performance as this would be run one time per system most of the time.
- Need to be able to add/modify package lists and configurations without much hassle.
- Preferably one script/executable for all. Soft requirement.

## Options:
- POSIX shell scripts with a Powershell variant for Windows.
    - This could have some kind of wrapper in something that could be run in any OS, like python.
- Compiled binary application. Target languages: C, C++, Go or Rust.
    - This approach can be truly cross-platform, although it'd require more work.
    - I would need to provide pre-compiled releases as I wouldn't want to do a lot of setup in order to build the tool.
        - Maybe Rust, with its one-liner installation could be a good enough compromise.
        - Another compromise would be, pre-stage the environment with a script.
    - I would also need an interface with the package managers used to install system-provided packages.
        - Probably could just spawn a new shell process and run through that.
- Python script from the get-go. Not as fun, but may be able to release something fast.

## Checklist:
- [ ] Main entrypoint
- [ ] Read from a package list
- [ ] Interface with package managers
    - [ ] Fedora: dnf
    - [ ] Ubuntu: apt
    - [ ] Windows: winget
    - [ ] Mac OS: brew
- [ ] Create directory structure
- [ ] Apply configurations
    - [ ] Integrate with my `dots` repo
- [ ] Install fonts
- [ ] Detect current state and apply changes accordingly
