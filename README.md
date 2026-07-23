<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>

<!-- /// d   u   b   p   i   x   e   l  ---  f   o   r   k   ////--v0.6.0 -->
<!--this has been modified by @dubpixel for 3D print project use -->
<!--search dpx_raxda_rockpis.. search & replace is COMMAND OPTION F -->

<!--this is the version for 3D projects -->

<!-- PROJECT SHIELDS -->
<div align="center">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]
</div>

<!-- PROJECT LOGO -->
<div align="center">
  <a href="https://github.com/dubpixel/dpx_raxda_rockpis">
    <img src="images/logo.png" alt="Logo" height="120">
  </a>
<h1 align="center">dpx_raxda_rockpis</h1>
<h3 align="center"><i>Custom POE enclosure for Radxa Rock Pi S</i></h3>
  <p align="center">
    3D print files for a compact two-part snap/bolt case housing the Rock Pi S + POE hat.
    Includes official Radxa reference models and the iterative DUBPixel case design (v8 → v14).
    <br />
     »  
     <a href="https://github.com/dubpixel/dpx_raxda_rockpis"><strong>Project Here!</strong></a>
     »  
     <br />
    <a href="https://github.com/dubpixel/dpx_raxda_rockpis/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    ·
    <a href="https://github.com/dubpixel/dpx_raxda_rockpis/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
    </p>
</div>
   <br />

<!-- TABLE OF CONTENTS -->
<details>
  <summary><h3>Table of Contents</h3></summary>
<ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#print-settings">Print Settings</a>
    </li>
    <li><a href="#usage">Usage</a></li>    
    <li><a href="#reflection">Reflection</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
</ol>
</details>

<!-- ABOUT THE PROJECT -->
<details>
<summary><h3>About The Project</h3></summary>
Custom two-part enclosure for the **Radxa Rock Pi S** single-board computer fitted with the **Rockpi POE HAT v1.2**. Designed so the whole stack — board, POE hat, and ethernet connector — sits cleanly inside a compact shell with no dangling cables.

The case went through several design iterations (v8 → v14) improving fitment, clearances for the POE hat capacitors, and the lid retention method. The final v14 STLs are the ones to print.

`src/reference/` contains the official Radxa STEP/DWG files used as the basis for each design revision. The custom case files live in `STL/`.

This project is used as the physical hardware platform for [dpx-buttnode](https://github.com/dubpixel/dpx_buttnode) — a flash-ready Armbian image for Bitfocus Buttons USB Relay + Companion Satellite.
</br>

*author(s): // www.dubpixel.tv  - i@dubpixel.tv*
</br>
<h3>Images</h3>

### FRONT
![FRONT][product-front]
</details>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

 * [![Fusion360][Fusion-360]][Autodesk-url]
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- PRINT SETTINGS -->
## Print Settings

| Setting | Value |
|---------|-------|
| Slicer | PrusaSlicer / Bambu Studio |
| Material | PLA |
| Layer Height | 0.2 mm |
| Infill | 20% gyroid |
| Supports | Yes — touching bed only (lid overhang and port cutouts) |
| Bed Adhesion | Brim (top/bottom pieces print separately) |
| Print Time | ~3h per piece @ 0.2mm |

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Usage

**Files to print** (use the latest revision — v14):
- `STL/dpx_rocpis_Poe_case_top_v14.stl`
- `STL/dpx_rocpis_Poe_case_bottom_v14.stl`

The `.3mf` assembly file (`STL/dpx_rocpis_Poe_case.3mf`) opens in PrusaSlicer / Bambu Studio with both parts pre-oriented.

1. Print top and bottom separately with supports touching bed only.
2. Seat the Rock Pi S board into the bottom shell — the board mounts on the standoff posts.
3. Stack the POE HAT onto the Rock Pi S 40-pin header.
4. Route the ethernet cable through the cutout in the back wall.
5. Press the top shell down until the lid clips engage. No fasteners needed on v14.

**Reference models** (`src/reference/`) are provided for context only — these are official Radxa STEP files used during design. You don't need them to print the case.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- REFLECTION -->
## Reflection

* what did we learn?
  - The POE HAT capacitors are taller than expected — early versions (v8/v10) had internal clearance issues that required iterating the lid height and internal rib positions.
  - Designing directly from the STEP reference files is far more reliable than calipers alone.
* what do we like/hate?
  - The clip retention on v14 is solid enough for a production node. No fasteners is the right call for a device that may need to be opened for USB swaps.
  - Ethernet port alignment was finicky across versions due to Rock Pi S PCB tolerance variance.
* what would/could we do differently?
  - A proper strain relief for the ethernet cable would be a good v15 addition.
  - Mounting holes for wall/rack mounting would make deployment cleaner.

<!-- ROADMAP -->
## Roadmap

- [ ] Feature 1
    - [ ] Nested Feature

See the [open issues](https://github.com/dubpixel/dpx_raxda_rockpis/issues) for a full list of proposed features (and known issues).

<!-- CONTRIBUTING -->
## Contributing

_Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**._

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Top contributors:
<a href="https://github.com/dubpixel/dpx_raxda_rockpis/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=dubpixel/dpx_raxda_rockpis" alt="contrib.rocks image" />
</a>

<!-- LICENSE -->
## License
Distributed under the [LICENSE_TYPE] License. See `LICENSE.txt` for more information.

<!-- CONTACT -->
## Contact

  ### Joshua Fleitell - i@dubpixel.tv

  Project Link: [https://github.com/dubpixel/dpx_raxda_rockpis](https://github.com/dubpixel/dpx_raxda_rockpis)

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

<!--
  * [ ]() - the best !
-->

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/dubpixel/dpx_raxda_rockpis.svg?style=flat-square
[contributors-url]: https://github.com/dubpixel/dpx_raxda_rockpis/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/dubpixel/dpx_raxda_rockpis.svg?style=flat-square
[forks-url]: https://github.com/dubpixel/dpx_raxda_rockpis/network/members
[stars-shield]: https://img.shields.io/github/stars/dubpixel/dpx_raxda_rockpis.svg?style=flat-square
[stars-url]: https://github.com/dubpixel/dpx_raxda_rockpis/stargazers
[issues-shield]: https://img.shields.io/github/issues/dubpixel/dpx_raxda_rockpis.svg?style=flat-square
[issues-url]: https://github.com/dubpixel/dpx_raxda_rockpis/issues
[license-shield]: https://img.shields.io/github/license/dubpixel/dpx_raxda_rockpis.svg?style=flat-square
[license-url]: https://github.com/dubpixel/dpx_raxda_rockpis/blob/main/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/jfleitell
[product-front]: images/front.png
[product-rear]: images/rear.png
[Fusion-360]: https://img.shields.io/badge/Fusion360-v4.2.0-green
[Autodesk-url]: https://autodesk.com
