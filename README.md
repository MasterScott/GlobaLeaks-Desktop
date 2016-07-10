GlobaLeaks Desktop Station is a tool for Journalists that want to safely and anonymously connect to a GlobaLeaks server.

If you are interested in helping out read the: [Request for Contributors](https://docs.google.com/document/d/1HgnfBd3apYxrORzXz72J8p9sILKd8DVKA6PlJ_6Xkh0/edit?usp=sharing)

### Requirements

- The application must be able to use Tor for all traffic.
- The applicaiton must use the existing frontend without needing significant modification
- The installation process must not be outside of the regular expectations
- The package delivered for installation must contain the whole application. (No bullshit with npm, brew, pip, apt-get, etc, etc)
- The data stored on the machine must live in one place.
- The build process must be reseanoable secure.

At the moment we are evaluating several ways to deliver this application.

#### Option 1

The application is a bundle of several technologies glued together:
 * Tor Browser Bundle (TBB) - https://www.torproject.org/projects/torbrowser.html.en
 * Firefox PGP encryption plug-in - https://github.com/kylehuff/webpg-npapi
 * A static angular application served from the user's machine.

#### Option 2
The application is a different set of bundled technologies:
 * Electron application framework with the webkit browser
 * A lightweight Tor SOCKS proxy

The GL Desktop provides the following features:
 * Web Browser is secured (hardened Aurora from TBB)
 * Anonimity is enforced through the use of Tor.
 * Private keys are kept offline until needed by the application

Usability improvements
 * Start page asking the user to:
  * Insert a GlobaLeaks site hostname
  * Browse/select a GlobaLeaks site from LeakDirectory.org
  * If the GL-Desktop is pre-configured, directly load the pre-configured GL site interface
 * TBD Windows Installer Usability Improvement

Security improvements
 * Strip down the browser functionality and user-interactions available
 * Support SNI for assets used locally.
 * Support pinned certificates for GL server (and certs for clients)
 * Identify a safe way to sandbox network requests used by Electron
 
Tor Integration Goals:
 * Whenever possible try to make major customizations (usability improvements & PGP Support) included into Tor Browser Bundle as a default feature set
  * Tor Talk PGP Plug-in Inclusion Mailing List Threads
   * https://lists.torproject.org/pipermail/tor-talk/2011-October/021627.html
   * https://lists.torproject.org/pipermail/tor-talk/2011-October/021642.html
  * Windows usability Improvements Mailing List Threads:
   * https://lists.torproject.org/pipermail/tor-talk/2011-October/021639.html


