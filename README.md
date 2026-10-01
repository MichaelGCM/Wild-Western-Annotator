# Blot Annotator — installers

Built installers for Blot Annotator, a desktop tool for arranging and annotating western blot and DNA gel images into publication-ready figures. The source code is private; this repository only hosts the downloads. Get the latest build from the [Releases page](https://github.com/MichaelGCM/blot-annotator-releases/releases).

## Installing on macOS

Download the release asset matching your Mac from the
[Releases page](https://github.com/MichaelGCM/blot-annotator-releases/releases), open it, and drag
**Blot Annotator** onto the **Applications** folder.

**Check the architecture in the filename.** Builds are per-architecture, not universal:
`BlotAnnotator-<version>-arm64.dmg` is for Apple Silicon (M1 and later) and
`BlotAnnotator-<version>-x86_64.dmg` is for Intel. An Apple Silicon Mac can run the Intel
build through Rosetta, but an Intel Mac **cannot** run the Apple Silicon build at all. Both
are published for every release, so pick the one matching your Mac — check
**Apple menu → About This Mac** if you aren't sure which you have.

**The first launch needs one extra step.** The app is not signed with an Apple Developer ID
and is not notarized — that requires a paid Apple Developer Program membership this project
doesn't have, and that is a permanent constraint rather than something coming later. macOS
will therefore refuse to open it on a plain double-click, saying it's from an unidentified
developer. Getting past that, once, depends on your macOS version:

**macOS 15 (Sequoia) and later** — the old right-click trick no longer works; the dialog has
no **Open** button at all:

1. Double-click **Blot Annotator**. macOS blocks it. Click **Done**.
2. Open **System Settings → Privacy & Security** and scroll to the **Security** section.
3. Next to "Blot Annotator was blocked…", click **Open Anyway**, then authenticate.

**macOS 14 (Sonoma) and earlier:**

1. Open your **Applications** folder in Finder.
2. **Right-click** (or Control-click) **Blot Annotator** and choose **Open**.
3. Click **Open** in the dialog that appears.

Either way macOS remembers the decision, and every launch after that is an ordinary
double-click. If you instead see "Blot Annotator is damaged and can't be opened", that is a
different problem — the download was corrupted, so re-download the `.dmg` rather than working
around it.

## Installing on Windows

Download `BlotAnnotator-<version>-windows-x64-setup.exe` from the
[Releases page](https://github.com/MichaelGCM/blot-annotator-releases/releases) and run it. You do
**not** need Python, and you do **not** need administrator rights — the app installs just for
you, under your own user folder.

**The first run needs one extra step.** The installer is not signed with an **Authenticode**
certificate — that requires a paid code-signing certificate this project doesn't have, and
that is a permanent constraint rather than something coming later. Windows will therefore
show a blue full-screen dialog reading **"Windows protected your PC"**:

1. Click **More info**.
2. Click **Run anyway**.
3. Follow the installer. It offers a desktop shortcut; a Start Menu entry is always created.

The app then launches from **Start → Blot Annotator**, and uninstalls from
**Settings → Apps → Installed apps → Blot Annotator**.

This warning is about reputation, not about anything being wrong with the download. Unlike
the macOS one above, it tends to disappear on its own once enough people have downloaded a
given release.

**64-bit Windows only.** If you are on a Windows-on-ARM machine, the installer still works —
Windows runs it under built-in emulation.

### Checking for updates

**Help → Check for Updates…** asks GitHub whether a newer release exists and, if so, offers
a link to its release page. It never downloads or installs anything by itself, and it only
runs when you ask it to — there is no background check.
