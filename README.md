# SpyOT-App

As part of the University of Nevada, Reno's Computer Science program, students are required to complete a senior
project. This project is a culmination of the skills and knowledge we have gained throughout the program.

This purpose of this repository is to house progress made among team members. The project itself is about identifying
vulnerabilities in IoT devices for small, local networks.

***

## Description

The SpyOT project is a network security tool that identifies vulnerabilities in a network of local IoT devices.
We attempt to tackle the beginning of a cybersecurity problem that users face when having a vast network of IoT devices.

## Requirements

- Windows 11
- [Nmap](https://nmap.org/download.html)

In order to use the SpyOT application, you will need to install the open-source network scanner, Nmap. Nmap can be
downloaded from https://nmap.org/download.html. Additionally, you will have to add the Nmap directory to your system's
PATH environment variable. Note that the nmap installer will automatically
add Nmap to the user PATH variable, but not the system PATH variable. Instructions on how to do this are available at
https://nmap.org/book/inst-windows.html for windows.

## Installation

### Executable

Once you have fulfilled the requirements above, you can download the SpyOT application from the releases page.
This will download a zip file containing the application. Extract the zip file to a location of your choice and run
main.exe to start the application.

### Source Code

If you would like to run the application from source code you will again need the above requirements filled, along with
Python 3.8 or higher. We recommend using a virtual environment to run the application and include a requirements.txt
file for your convenience. To install the required packages, run the following command from the root directory of the
project:

```
pip install -r requirements.txt
```

Once the packages are installed, you should be able to start the application by running the main.py file in the projects
root directory with the following python command.
    
```
python main.py
```

## Usage

![Home Screen](https://github.com/SpyOT/SpyOT-App/blob/main/images/Home_Screen.png?raw=true)

The application has 3 main use cases:

1. Scanning and identifying IoT devices in a network
2. Identify vulnerabilities in IoT devices
3. Generate a report detailing those findings

An experimental feature of this application is the ability to upload a vulnerability report to an online database
through an account linked to the SpyOT website. This feature is not fully implemented and is not recommended for use.

### Scanning

![Output of scan button](https://github.com/SpyOT/SpyOT-App/blob/main/images/Scan_Output.png?raw=true)

Perform a light-weight scan on your
systems with the help of the Nmap library. Once complete,
a list containing all devices on your systems will
be displayed on the right-hand display.

### Vulnerability Identification

![Output of collect button](https://github.com/SpyOT/SpyOT-App/blob/main/images/Collect_Output.png?raw=true)

Perform a deep scan of your systems
that allows it to collect information on each devices ports
including: protocol, availability, and service. At this point
you may also blacklist specific devices by clicking on
the devices name, then selecting the 'Add to blacklist' button.
You may also remove that device from your blacklist by
selecting the 'Remove from blacklist' button.

### Report Generation

![Output of view report button](https://github.com/SpyOT/SpyOT-App/blob/main/images/Report_Output.png?raw=true)

Generate a vulnerability report for your network after performing a
deep scan. This report will contain information on each device including:
IP address, MAC address, and open ports. This report will also contain
information on each port including: protocol, availability, and service.

## Original Project Proposal

For this senior project, we attempt to tackle the beginning of a cybersecurity problem that user networks face when
having a vast IoT environment that malicious software can manipulate and take advantage of by informing the user of the
threats that are associated with the vulnerabilities of their network. In order to inform the user, first we need to
identify connected IoT devices that are on a user’s network. Once those devices are detected and the data is compiled
into a list or graph, there needs to be a simple and easy to understand way of displaying that information of the
detected devices to the user so that the user can understand which devices are at risk of malicious software. As the
user is informed of their at-risk devices, then the user can begin the steps towards improving their network security in
order to prevent malicious software from attaching themselves to their network of IoT devices.

Our project’s mission towards network security is to improve a user’s network. To improve the user’s network, a layer of
security can be provided by supplying the user readable knowledge of their network’s vulnerabilities towards bad-agents
that use malware and malicious software to access that user’s network. If that user is able to see their network,
understand and utilize what information they have then the project has successfully completed its mission.

With the amount of IoT environments that are available to the non-technical public comes the great need for security and
a way to monitor that environment. Our project will provide that peace of mind that users with non-technical knowledge
will likely desire without taking a more expensive route for security measures on just detecting vulnerabilities and
threats.
