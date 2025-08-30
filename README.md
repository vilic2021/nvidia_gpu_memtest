`NVIDIA GPU Diagnostic Tool 🛠️
A professional tool for comprehensive diagnostics of NVIDIA graphics cards, supporting architectures from Fermi to Pascal.

✨ Features

Full Memory Testing – 16+ verification algorithms with detailed error analysis

Built-in Self-Test (BIST) – Utilizes GPU hardware self-testing capabilities

Real-Time Monitoring – Tracks temperature, power usage, and memory status

ECC Diagnostics – Detects and analyzes memory correction errors

Cross-Architecture Support – Works with Fermi, Kepler, Maxwell, and Pascal GPUs

Detailed Reporting – Full statistics and actionable recommendations

📋 Supported Hardware

GPU Architectures

Fermi (GTX 500 series)

Kepler (GTX 600/700 series)

Maxwell (GTX 900 series)

Pascal (GTX 1000 series)

System Requirements

Linux (Ubuntu 18.04+, Debian 10+, CentOS 7+)

NVIDIA GPU with 1GB+ VRAM

Superuser (root) privileges

GCC 7.0+ and development tools

🚀 Quick Start

Install Dependencies

Ubuntu/Debian
sudo apt update
sudo apt install build-essential linux-headers-$(uname -r)

CentOS/RHEL
sudo yum groupinstall "Development Tools"
sudo yum install kernel-devel

Compile the Project

Optimized build
gcc -o nvidia_diag nvidia_diag.c -O2 -lpthread -lrt -lm

Check the build
chmod +x nvidia_diag
./nvidia_diag --version

Basic Usage

Full diagnostic (recommended)
sudo ./nvidia_diag --full

Save results to file
sudo ./nvidia_diag --full --log diagnostic_report.txt

Quick memory check
sudo ./nvidia_diag --memory --quick

📊 Operating Modes

Primary Commands

Comprehensive diagnostics
sudo ./nvidia_diag --full

Memory test with detailed analysis
sudo ./nvidia_diag --memory --pattern all

Run built-in GPU tests (BIST)
sudo ./nvidia_diag --bist

Real-time monitoring
sudo ./nvidia_diag --monitor --interval 2

Generate report
sudo ./nvidia_diag --report --output report.html

Command-Line Parameters

Parameter Description Default
--full Full diagnostics ✅
--memory Memory test
--bist BIST testing
--monitor Monitoring mode
--quick Quick mode
--verbose Verbose output
--log Save log to file
--interval Monitoring interval (in seconds) 5
🔧 Technical Details

Memory Testing Algorithms
The tool uses 16+ patterns for comprehensive memory checking:

Basic patterns: All zeros/ones, Alternating bits

Structural patterns: Incremental, Decremental

Stress patterns: Dead beef, Cafe babe, Complex patterns

Specialized: Walking ones/zeros, Nybble patterns

System Monitoring

GPU Temperature – Overheating control

Power Consumption – Load analysis

ECC Statistics – Memory correction error logs

Clock Frequencies – Core operation monitoring

📈 Result Interpretation

Error Levels

Level Description Recommendation
INFO Informational message Monitoring
WARNING Minor issues Check cooling system
ERROR Critical errors Hardware diagnostics
CRITICAL Hardware failure Replace components

Sample Report

=== DIAGNOSTIC REPORT ===
GPU: GeForce GTX 1080 (Pascal)
Test duration: 45.2 seconds
Memory tested: 8192 MB

STATISTICS:

Total tests: 1,500,000
Memory errors: 12 (0.0008%)
ECC corrected: 8
ECC uncorrected: 0
Max temperature: 78°C
RECOMMENDATIONS:
✅ Memory integrity: Excellent
⚠️ Monitor temperature under load
🔧 Consider cleaning cooling system

⚠️ Important Notices

Safety Information

Root access is required for hardware testing
May cause system instability during tests
Close all applications before running tests
Always back up important data
Limitations

Linux-only

Requires physical GPU access

Supports up to Pascal architecture only

No multi-GPU support

🐛 Troubleshooting

Common Issues

Hardware access error
sudo ./nvidia_diag

GPU not detected
Check architecture support
Compilation errors
Ensure build-essential is installed
Debug Mode

Verbose output with debug info
sudo ./nvidia_diag --verbose --debug

Log output to file
sudo ./nvidia_diag --log debug.log --verbose

📝 Usage Examples

Preventive Diagnostics

Monthly system check
sudo ./nvidia_diag --full --log monthly_check.txt

Problem Diagnosis

When artifacts appear
sudo ./nvidia_diag --memory --pattern stress

If overheating occurs
sudo ./nvidia_diag --monitor --interval 1

Production Testing

Full server-side test
sudo ./nvidia_diag --full --bist --log production_test.txt

🔄 Comparison With Alternatives
Feature This Tool MATS
Memory Tests 16+ patterns 3–4 patterns
ECC Monitoring Real-time Post-factum
Reporting Detailed statistics Error codes
Monitoring Temp/Power Not supported
Safety State preservation Direct hardware access
📞 Support

Reporting Issues

Run with --verbose --debug

Save output: --log error_report.txt

Include GPU model and driver version

Questions & Suggestions

Check the documentation and existing issues

Use templates for bug reports

Feature suggestions are welcome

📜 License

This project is licensed under the MIT License. Full text available in the LICENSE file.

⚠️ Disclaimer

This tool is intended for diagnostic use only. The authors are not responsible for any hardware damage or data loss. Use at your own risk.

Test on non-critical systems before using in production.
`

⚠️ Project Status
Discontinued — This project is no longer active.
It was closed due to limited time and technical challenges beyond current expertise.
Feel free to fork or explore the code for reference.



Thank you for your interest in the project!

Unfortunately, this project is currently on hold due to:

Limited time for proper development
Technical complexities with low-level GPU access
Lack of necessary documentation for NVIDIA hardware
I may revisit it in the future when I have more experience with:

DOS programming
PCI/MMIO hardware access
NVIDIA's internal architecture
Feel free to fork the repository if you want to experiment with the code!
