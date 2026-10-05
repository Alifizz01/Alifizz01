<img src="assets/banner.svg" alt="Alif Izzuwan: electrical engineering and electromobility" width="100%">

I build the tools I wish test benches came with. My B.Eng. in electrical engineering and electromobility at
TH Ingolstadt ended with a thesis that reads a VW ID. Buzz's battery through the OBD-II gateway, and an internship
on a hardware-in-the-loop test team showed me how much time engineers lose to missing tooling. Most of what is
below comes from one of those two places: **vehicle networks, battery systems, and the software and hardware
that test them.**

### Automotive diagnostics & testing

<table>
<tr>
<td width="50%" valign="top">
<img src="assets/icon-thesis.svg" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/CANedge2-UDS-implementation-Thesis">VW ID. Buzz battery over UDS</a></b> · bachelor thesis<br>
<sub>The MEB gateway hides the BMS from the OBD-II port, so a CANedge2 logger <i>asks</i> instead of listens. 60 identifiers tested,
three encodings the public list gets wrong, and a desktop app for logger profiles and MF4 decoding.</sub><br>
<sub><code>CAN</code> <code>UDS</code> <code>Python</code> <code>LaTeX</code></sub>
</td>
<td width="50%" valign="top">
<img src="https://raw.githubusercontent.com/Alifizz01/XiLoop/main/assets/logo-mark.png" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/XiLoop">XiLoop</a></b> · X-in-the-loop test bench<br>
<sub>One test plan from a Python prototype to C firmware to a real board: SiL, PiL and HiL with the same
requirements, a desktop studio and a REST API.</sub><br>
<sub><code>Python</code> <code>C</code> <code>control</code> <code>HiL</code></sub>
</td>
</tr>
<tr>
<td valign="top">
<img src="https://raw.githubusercontent.com/Alifizz01/BusBench/main/assets/logo-mark.png" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/BusBench">BusBench</a></b> · protocol workbench<br>
<sub>Ten automotive and avionics protocols (CAN, UDS/ISO-TP, AUTOSAR, DoIP, ARINC 429, MIL-STD-1553 …) implemented
twice, in C and in Python, and tested against each other. Fuzzed in CI.</sub><br>
<sub><code>C</code> <code>Python</code> <code>libFuzzer</code></sub>
</td>
<td valign="top">
<img src="assets/icon-toolbridge.svg" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/ToolBridge">ToolBridge</a></b> · APIs for GUI-only tools<br>
<sub>Reads a Windows engineering tool (an ECU flasher, a calibration program) through UI Automation and .NET
metadata and generates a Python package and REST API for it. No pixel clicking.</sub><br>
<sub><code>Python</code> <code>UI Automation</code> <code>.NET</code></sub>
</td>
</tr>
<tr>
<td valign="top">
<img src="https://raw.githubusercontent.com/Alifizz01/BenchPulse/main/assets/logo-mark.png" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/BenchPulse">BenchPulse</a></b> · HiL lab dashboard<br>
<sub>Which bench PC is free, who is on the busy ones over Remote Desktop, and when you can book it.
One browser page for the whole lab, no install for colleagues.</sub><br>
<sub><code>Python</code> <code>Windows API</code> <code>SQLite</code></sub>
</td>
<td valign="top">
<img src="assets/icon-pilink.svg" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/PiLink">PiLink</a></b> · verified PC ↔ USB transfer box<br>
<sub>A Raspberry Pi between a locked-down PC and a USB stick: the PC only speaks FTP, every copy is
checksum-verified before it says "done".</sub><br>
<sub><code>Python</code> <code>Raspberry Pi</code></sub>
</td>
</tr>
</table>

### Battery & powertrain

<table>
<tr>
<td width="50%" valign="top">
<img src="https://raw.githubusercontent.com/Alifizz01/GAIA/main/assets/logo-mark.png" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/GAIA">GAIA</a></b> · BMS simulator<br>
<sub>PyBaMM electrochemistry for the cells and a real BMS on top: SOC estimation, protection, balancing,
contactors. Fault injection, a desktop studio and Simulink blocks.</sub><br>
<sub><code>Python</code> <code>PyBaMM</code> <code>MATLAB/Simulink</code></sub>
</td>
<td width="50%" valign="top">
<img src="assets/icon-aether.svg" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/AETHER">AETHER</a></b> · electric propulsion<br>
<sub>GAIA's sibling for what the battery drives: give it a throttle and get the whole chain, from where the
shaft settles to where every watt went.</sub><br>
<sub><code>Python</code> <code>modelling</code></sub>
</td>
</tr>
</table>

### Hardware

<table>
<tr>
<td width="50%" valign="top">
<img src="assets/icon-fpga.svg" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/fpga-can-timestamper">CAN-FD hardware timestamper</a></b> · FPGA<br>
<sub>A two-channel CAN-FD receiver in VHDL that timestamps every frame in hardware on one shared clock. Open
toolchain rebuilt in CI, with a <a href="https://alifizz01.github.io/fpga-can-timestamper/">live capture viewer</a>.</sub><br>
<sub><code>VHDL</code> <code>Lattice ECP5</code> <code>CAN-FD</code></sub>
</td>
<td width="50%" valign="top">
<img src="assets/icon-pcb.svg" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/automotive-pcb-portfolio">Automotive PCB portfolio</a></b> · Altium<br>
<sub>Three CAN-FD tools taken end to end: requirements, schematic, layout, fab outputs. A sniffer HAT for the Pi
Zero 2 W, a handheld OBD-II test runner, and an isolated FPGA timestamper board.</sub><br>
<sub><code>Altium Designer</code> <code>CAN-FD</code> <code>Raspberry Pi</code></sub>
</td>
</tr>
</table>

### Desktop

<table>
<tr>
<td width="50%" valign="top">
<img src="https://raw.githubusercontent.com/Alifizz01/Floatie/master/assets/logo-mark.png" width="44" align="left" hspace="10">
<b><a href="https://github.com/Alifizz01/Floatie">Floatie</a></b> · desktop fences for Windows<br>
<sub>Live, filtered views of your Desktop and Downloads that stay where you put them, plus a Tidy with preview and
undo. About 10 MB of RAM idle.</sub><br>
<sub><code>C#</code> <code>WPF</code> <code>Win32</code></sub>
</td>
</tr>
</table>

### Toolbox

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?logo=c&logoColor=white)
![C#](https://img.shields.io/badge/C%23%20%2F%20.NET-512BD4?logo=dotnet&logoColor=white)
![VHDL](https://img.shields.io/badge/VHDL-1B2430)
![MATLAB](https://img.shields.io/badge/MATLAB%20%2F%20Simulink-E16737)
![Altium](https://img.shields.io/badge/Altium%20Designer-A5915F)
![CAN](https://img.shields.io/badge/CAN%20%C2%B7%20CAN--FD%20%C2%B7%20UDS-3DBFA7)
![LaTeX](https://img.shields.io/badge/LaTeX-008080?logo=latex&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?logo=githubactions&logoColor=white)
