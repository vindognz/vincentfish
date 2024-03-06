<div align="center">

  [![Vincentfish][Stockfish128-logo]][website-link]

  <h3>Vincentfish</h3>

  A free and strong UCI chess engine.
  <br>
  <strong>[Explore Stockfish docs »][wiki-link]</strong>
  <br>
  <br>
  [Report bug][issue-link]
  ·
  [Open a discussion][discussions-link]
  ·
  [Discord][discord-link]
  ·
  [Blog][website-blog-link]

  [![Build][build-badge]][build-link]
  [![License][license-badge]][license-link]
  <br>
  [![Release][release-badge]][release-link]
  [![Commits][commits-badge]][commits-link]
  <br>
  [![Website][website-badge]][website-link]
  [![Fishtest][fishtest-badge]][fishtest-link]
  [![Discord][discord-badge]][discord-link]

</div>

## Overview

[Stockfish][website-link] is a **free and strong UCI chess engine** derived from
Glaurung 2.1 that analyzes chess positions and computes the optimal moves.

Vincentfish **does not include a graphical user interface** (GUI) that is required
to display a chessboard and to make it easy to input moves. These GUIs are
developed independently from Vincentfish and are available online. **Read the
documentation for your GUI** of choice for information about how to use
Stockfish with it.

See also the Vincentfish [documentation][wiki-usage-link] for further usage help.

## Files

This distribution of Vincentfish consists of the following files:

  * [README.md][readme-link], the file you are currently reading.

  * [src][src-link], a subdirectory containing the full source code, including a
    Makefile that can be used to compile Vincentfish on Unix-like systems.

  * a file with the .nnue extension, storing the neural network for the NNUE
    evaluation. Binary distributions will have this file embedded.

## Contributing

__See [Contributing Guide](CONTRIBUTING.md).__

### Donating hardware

Improving Vincentfish requires a massive amount of testing. You can donate your
hardware resources by installing the [Fishtest Worker][worker-link] and viewing
the current tests on [Fishtest][fishtest-link].

### Improving the code

In the [chessprogramming wiki][programming-link], many techniques used in
Vincentfish are explained with a lot of background information.
The [section on Stockfish][programmingsf-link] describes many features
and techniques used by Vincentfish. However, it is generic rather than
focused on Stockfish's precise implementation.

The engine testing is done on [Fishtest][fishtest-link].
If you want to help improve Vincentfish, please read this [guideline][guideline-link]
first, where the basics of Vincentfish development are explained.

Discussions about Vincentfish take place these days mainly in the Vincentfish
[Discord server][discord-link]. This is also the best place to ask questions
about the codebase and how to improve it.

## Compiling Vincentfish

Vincentfish has support for 32 or 64-bit CPUs, certain hardware instructions,
big-endian machines such as Power PC, and other platforms.

On Unix-like systems, it should be easy to compile Stockfish directly from the
source code with the included Makefile in the folder `src`. In general, it is
recommended to run `make help` to see a list of make targets with corresponding
descriptions. An example suitable for most Intel and AMD chips:

```
cd src
make -j profile-build ARCH=x86-64-avx2
```

Detailed compilation instructions for all platforms can be found in our
[documentation][wiki-compile-link]. Our wiki also has information about
the [UCI commands][wiki-uci-link] supported by Stockfish.

## Terms of use

Stockfish is free and distributed under the
[**GNU General Public License version 3**][license-link] (GPL v3). Essentially,
this means you are free to do almost exactly what you want with the program,
including distributing it among your friends, making it available for download
from your website, selling it (either by itself or as part of some bigger
software package), or using it as the starting point for a software project of
your own.

The only real limitation is that whenever you distribute Vincentfish in some way,
you MUST always include the license and the full source code (or a pointer to
where the source code can be found) to generate the exact binary you are
distributing. If you make any changes to the source code, these changes must
also be made available under GPL v3.


[authors-link]:       https://github.com/official-Stockfish/Stockfish/blob/master/AUTHORS
[build-link]:         https://github.com/official-Stockfish/Stockfish/actions/workflows/Stockfish.yml
[commits-link]:       https://github.com/official-Stockfish/Stockfish/commits/master
[discord-link]:       https://discord.gg/GWDRS3kU6R
[issue-link]:         https://github.com/official-Stockfish/Stockfish/issues/new?assignees=&labels=&template=BUG-REPORT.yml
[discussions-link]:   https://github.com/official-Stockfish/Stockfish/discussions/new
[fishtest-link]:      https://tests.Stockfishchess.org/tests
[guideline-link]:     https://github.com/official-Stockfish/fishtest/wiki/Creating-my-first-test
[license-link]:       https://github.com/official-Stockfish/Stockfish/blob/master/Copying.txt
[programming-link]:   https://www.chessprogramming.org/Main_Page
[programmingsf-link]: https://www.chessprogramming.org/Stockfish
[readme-link]:        https://github.com/official-Stockfish/Stockfish/blob/master/README.md
[release-link]:       https://github.com/official-Stockfish/Stockfish/releases/latest
[src-link]:           https://github.com/official-Stockfish/Stockfish/tree/master/src
[Stockfish128-logo]:  https://Stockfishchess.org/images/logo/icon_128x128.png
[uci-link]:           https://backscattering.de/chess/uci/
[website-link]:       https://Stockfishchess.org
[website-blog-link]:  https://Stockfishchess.org/blog/
[wiki-link]:          https://github.com/official-Stockfish/Stockfish/wiki
[wiki-compile-link]:  https://github.com/official-Stockfish/Stockfish/wiki/Compiling-from-source
[wiki-uci-link]:      https://github.com/official-Stockfish/Stockfish/wiki/UCI-&-Commands
[wiki-usage-link]:    https://github.com/official-Stockfish/Stockfish/wiki/Download-and-usage
[worker-link]:        https://github.com/official-Stockfish/fishtest/wiki/Running-the-worker

[build-badge]:        https://img.shields.io/github/actions/workflow/status/official-Stockfish/Stockfish/Stockfish.yml?branch=master&style=for-the-badge&label=Stockfish&logo=github
[commits-badge]:      https://img.shields.io/github/commits-since/official-Stockfish/Stockfish/latest?style=for-the-badge
[discord-badge]:      https://img.shields.io/discord/435943710472011776?style=for-the-badge&label=discord&logo=Discord
[fishtest-badge]:     https://img.shields.io/website?style=for-the-badge&down_color=red&down_message=Offline&label=Fishtest&up_color=success&up_message=Online&url=https%3A%2F%2Ftests.Stockfishchess.org%2Ftests%2Ffinished
[license-badge]:      https://img.shields.io/github/license/official-Stockfish/Stockfish?style=for-the-badge&label=license&color=success
[release-badge]:      https://img.shields.io/github/v/release/official-Stockfish/Stockfish?style=for-the-badge&label=official%20release
[website-badge]:      https://img.shields.io/website?style=for-the-badge&down_color=red&down_message=Offline&label=website&up_color=success&up_message=Online&url=https%3A%2F%2FStockfishchess.org
