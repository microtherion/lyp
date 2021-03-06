# Version 1.3.11 2018-02-13

- Remove self-contained releases.
- Update rugged dependency (#64)
- Fix install script (#65)
- Introduce new commands for requiring packages and including files (#61).

# Version 1.3.8 2018-02-05

- Fix Lilypond installation link (the  http://download.linuxaudio.org/lilypond links don't work anymore).

# Version 1.3.7 2018-01-22

- Fix installation of non-registered github packages (#54).
- Set default encoding to UTF-8 (#52).
- Fix Lilypond install on Windows.
- Accept symbol arguments for require, include commands (#49).
- Improve docs.

# Version 1.3.5 2017-01-16

- Add `--svg` command line option (#50).
- Improve Lilypond commandline option parsing.
- Remove non-functional `--open` switch.
- Improve error reporting (print backtrace only when `--verbose` is specified).
- Add `--music`/`--music-relative` command line switch for quickly entering music on the command line (#47).

# Version 1.3.4 2017-01-09

- Recover from trying to open broken Lilypond archives.
- Trap INT signals.
- Better documentation ([new website](http://lyp.noteflakes.com/)).

# Version 1.3.3 2017-01-03

- Properly suport stock include in flatten (#45).

# Version 1.3.2 2017-01-03

- Fix stock Lilypond includes, include search path (#44, #43).
- Remove rugged dependency from traveling ruby release.
- Fix install script to work with wget (#41).

# Version 1.3.1 2016-12-26

- Add `lyp benchmark` command (#17).
- Add shortcuts for common commands.
- Add `lyp watch` command (#38).

# Version 1.2.1 2016-12-21

- Fix `lyp test --env` command.

# Version 1.2.0 2016-12-21

- Implement `lyp accelerate` command for making lyp and Lilypond scripts faster (#34).
- Add `lyp exec` command for running arbitrary Lilypond bundled scripts (#35).

# Version 1.1.0 2016-12-04

- Improve performance by loading dependencies only when needed.
- Implement `lyp update` and `lyp install -u` commands (#33).

# Version 1.0.3 2016-11-30

- Refactor Lilypond option parsing.
- Refactor version and version requirement construction.

# Version 1.0.2 2016-11-28

- Add support for finalizers in package Scheme API.
- Fix ARGV parsing when filename includes hyphen.
- Better documentation for Ruby extension API.

## Version 1.0.1 2016-08-31

- Better error reporting when installing packages.
- Add appropriate `\paper` preamble when `--snippet` option is specified (#29).
- Improve Lilypond option processing by allowing a string of single-letter options, e.g. `lilypond -FncO`.
- Add `--force-version` Lilypond option for selecting Lilypond version according to version statement in user file (#28).

## Version 1.0.0 2016-06-29

- Fix `\pcondIncludeOnce`.
- Implement flatten command (#26).

## Version 0.3.9 2016-06-27

- Add `--auto-install-deps` Lilypond option for automatically installing missing dependencies (#25).
- Add `--snippet` option to Lilypond for creating cropped png images (#24).
- Add `--dev` option for installing development packages (#23).
- Raise error in mismatching require version clauses in same file (#12).
- Add automatic periodic checking for new unstable versions of Lilypond (#7).

## Version 0.3.8 2016-06-14

- Fix behavior when `-dhelp` switch is specified.
- Add custom `-c, --cropped` switch for cropped Lilypond output (shorthand for `-dbackend=eps -daux-files=#f`).
- Fix installing font packages with nested font directories.

## Version 0.3.7 2016-06-02

- Update package URLs (packages are now placed in the [lyp-packages](https://github.com/lyp-packages) organisation).
- Run *-test.ly as well as *_test.ly files.
- Show assert summary if assert package was loaded.
- Add `\pcondInclude`, `\pcondIncludeOnce` commands for conditional includes.

## Version 0.3.6 2016-03-08

- Add `-r/--require` command line for preloading packages (#19).
- Rewrite `\require`, `\pinclude`, `\pincludeOnce` commands for better compatibility with legacy Lilypond code.

## Version 0.3.5 2016-03-01

- Ask for confirmation before patching and installing fonts in system-installed Lilyponds.

## Version 0.3.4 2016-02-29

- Make lyp and Lilypond binaries load faster.
- Fix installing fonts for system-installed Lilyponds (#18).
- Show package description on search.

## Version 0.3.3 2016-02-21

- Add support for including ruby extensions in packages.
- Rewrite package scheme interface, \pinclude now properly supports relative paths when doing nested includes, on both Lilypond 2.18 and 2.19.

## Version 0.3.2 2016-02-20

- Fix --raw command line option in Lilypond binary script.
- Wrap also files without package dependencies, in order to provide the \pinclude, etc. functionality. This can be overriden using the --raw command line option.

## Version 0.3.1 2016-02-04

- Accept stdin input for Lilypond.
- Show `install self` warning only for standalone releases.

## Version 0.3.0 2016-02-03

- Improve `lyp install self` behavior on all platforms.
- Add standalone package for Windows.

## Version 0.2.3 2016-02-02

- Windows support!

## Version 0.2.2 2016-01-31

- Improve README documentation.
- Fix Lilypond wrapper to not eat stock Lilypond options (#10).
- Add --env, --use, --install options to Lilypond wrapper, lyp test, lyp compile commands.
- Remove nokogiri dependency.
- Fix behaviour when no version of Lilypond is installed.
- Various improvements to command line interface.

## Version 0.2.1 2016-01-28

- Packages tests can now use `\require "<package name>:<relative path>"` syntax in tests to make sure tests work anywhere. For an example see the [assert package](https://github.com/noteflakes/lyp-assert).
- Complete rewrite of package scheme interface, now tested using the assert package.

## Version 0.2.0 2016-01-27

- Rename `lyp-*` variables to `lyp:*`.
- Add -t switch to `lyp install` to test a package after installation.
- Fix uninstalling non-versioned packages.
- Add `lyp test` command for testing packages.
- Fix `lyp install` command.
- Fix and enhance `lyp compile` command.
- Fix `lyp uninstall self` command.
- Accept `scheme-sandbox` argument in Lilypond wrapper (#8).
- Add support for installing custom fonts from packages (starting from Lilypond 2.18.2), and automatic patching of Lilypond versions lower than 2.19.12 in order to support custom fonts.

## Version 0.1.4 2016-01-24

- Fix lyp-current-package-dir for local (development) packages.

## Version 0.1.3 2016-01-24

- Do not list Lilypond script in Gem bindir (#6).
- Add lyp-* variables, \pinclude command for including files from within packages.
- Add [installation script](https://github.com/noteflakes/lyp#installation).

## Version 0.1.2 2016-01-18

- Add stand-alone release using [traveling-ruby](https://github.com/phusion/traveling-ruby).

## Version 0.1.0 2016-01-13

- Improve output of `lyp list` (group by package).
- Display warning, do not exit if lyp self installation test fails.
- Fix install/uninstall using git URL.
- Add support for installing a package from local files:

    lyp install mypack@dev:~/repo/mypack

- Add resolve command to install all dependencies required for a given .ly file.
- Add deps command to show required dependencies for a given .ly file.
- Ampersand can be ommited when specifying version constraints, e.g. `lilypond>=2.19.31` etc.

## Version 0.0.5 2016-01-11

- Add which command (for both packages and Lilypond).
- Add package uninstall command.
- Check validity of default/current Lilypond before invoking it.
- Install highest versioned tag if version is not specified.
- CLI now uses thor for prettier code.
- Fix bin/lilypond to work with multiple arguments.

## Version 0.0.4 2016-01-10

- Search for simple package name (non-url) in [lyp-index](https://github.com/noteflakes/lyp-index).
- Add support for `lyp search lilypond@<version|stable|unstable|latest>`.
- Implement package installation.
- Move lyp repository to [noteflakes org](https://github.com/noteflakes/lyp).

## Version 0.0.3 2016-01-08

- Add uninstall lyp command.
- Add install lyp command.
- Cleanup temp files in /tmp after installing Lilypond.
- Add support for 'lyp install lilypond' (install latest stable version).

## Version 0.0.2 2016-01-07

- Install, uninstall and switch between different versions of Lilypond.
- Resolve package dependencies in user files, and invoke Lilypond.
