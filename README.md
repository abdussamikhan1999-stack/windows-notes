# Windows (/fwt/) Notes

Notes distilled from `/fwt/` (Friendly Windows Thread, 4chan `/g/`-style).

See [LINKS.md](LINKS.md) for the raw link list.

## A flag before the summary

Most of this thread's content is about **activating Windows and Office
without a paid license** (an activation-bypass tool, plus pastebins linking
to Windows/Office ISOs) and about running de-bloated LTSC editions on top of
that. Unlike the other `/g/`-general repos in this series (browsers, PC
parts, image-gen tools), this isn't a neutral tool/resource recommendation —
using these to activate real installs is a license-terms violation
(Microsoft's EULA), regardless of how normalized it is in enthusiast
circles. So: what follows documents *what the thread says*, not a
step-by-step I'm walking you through — I've deliberately left out the
literal activation command and ISO-download specifics. If you want a
licensed Windows install, that's a Microsoft Store / retail-key purchase,
not something in this repo.

## What LTSC actually is (the legitimate, factual part)

**LTSC (Long-Term Servicing Channel)** is a real Microsoft product line, not
a piracy thing in itself — it's Microsoft's own "no feature updates, security
patches only, long support window" edition, originally meant for embedded/
industrial systems that can't tolerate Windows' normal churn. That's why
enthusiasts want it on a desktop: no Store, no bundled apps (no Candy Crush,
etc.), no forced feature-upgrade churn, longer support windows than
consumer editions.

- **W10 Enterprise IoT LTSC 2021** — binary-identical to normal Enterprise
  minus Store/bundled apps; supported to 2032 (the plain non-IoT LTSC SKU
  is supported only to 2027 — IoT LTSC gets a longer window for the same
  underlying build).
- **W11 Enterprise IoT LTSC 2024** — same idea on Windows 11; notably its
  Start menu/Taskbar/Explorer UI is built in React Native (JavaScript), not
  native code. The thread's own framing: only bother with W11 LTSC if you
  specifically need the newer Intel 12th-gen+ CPU thread-scheduling
  support that W10 lacks — otherwise W10 LTSC 2021 is the simpler choice.
- **W11 Enterprise IoT LTSC 2027** (future, ~2027H2) — same lineage, but
  the UI is being rewritten again in native WinUI instead of React Native.
- **Consumer editions (Home/Pro/Education/Enterprise/Enterprise IoT
  non-LTSC)** — the normal fast-moving channel: Store, bundled apps that
  reinstall themselves on feature updates, 1.5–3 years of support, and
  forced version upgrades. This is what LTSC exists specifically to avoid.

## App installation on a debloated LTSC install

Since LTSC ships without the Microsoft Store, the thread recommends
**WinGet** or **Scoop** (both legitimate, standard Windows package
managers — nothing piracy-adjacent about either) for installing normal
software, or re-enabling the Store itself via `wsreset -i` in an admin
Command Prompt if you want it back.

## "I miss old Windows" — UI nostalgia tools

**OpenShell**, **RetroBar**, **WinClassic**, **StartIsBack** — all
legitimate, standalone UI-customization tools (not activation/piracy
related) that restore older-Windows-style Start menus/taskbars on modern
Windows. Fine to use regardless of how you obtained your Windows license.

## Building/debloating your own ISO

The thread explicitly gatekeeps this: **"If you need to ask, then no"** —
i.e., don't attempt custom ISO debloating unless you already understand
what you're doing, since a botched debloat script can strip components
Windows actually needs. Reasonable advice independent of the piracy angle.

## Install guides (rentry)

Several rentry.org guides are linked for the LTSC install process
end-to-end (`windowsinstallguide`, `concisewin10`, `ltsc`, `fwtarchive`) —
these mix legitimate install/configuration steps with the activation-bypass
step discussed above; use your own judgment on which parts you actually
want to follow.
