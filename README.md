# NMAP-GPT

![nmap-gpt](https://github.com/tadmonyayafranklin/NmapGPT-/blob/main/08fbacbd4a381e7db2a83b9aad5eb15c_high.webp)

This tool helps security professionals actively learn how to address security concerns associated with open ports on a network device. It works by scanning the device using Nmap and then leveraging the OpenAI API to provide insights on specific security considerations for each open port, including the latest vulnerability information as of 2025.

## Features

- **Modern OpenAI API**: Updated to use the latest OpenAI client library and models
- **Enhanced Scanning**: Added advanced scanning options for more detailed vulnerability assessment
- **Comprehensive Reports**: Detailed reports with service version detection and OS fingerprinting
- **Export Options**: Save results in JSON or CSV format for further analysis

## Installation

1. Install required dependencies:

```bash
pip install python-nmap openai
```


2. Set your OpenAI API key:

```bash
export OPENAI_API_KEY="your-api-key-here"
```

## Usage

### Basic Nmap Scan

```bash
python3 nmap-gpt.py example.com -p 80
```

### Advanced Nmap Scan with Version Detection

```bash
python3 nmap-gpt.py example.com -p 1-1000 --scan-type advanced --output results.json
```

## Command Options

### Nmap-GPT Options

```
  host                  Host or IP address to scan
  -p PORT, --port PORT  Port or port range to scan (default: '1-1024')
  --output OUTPUT       Output file to save results (JSON or CSV)
  --model MODEL         OpenAI model to use (default: 'gpt-4-turbo')
  --scan-type {basic,advanced}
                        Type of scan to perform (default: 'basic')
```

## Examples 

### Basic Port Scanning

![Example of basic port scan](https://user-images.githubusercontent.com/63926014/218787405-c4fdd27d-06b6-44e6-ae97-174033dd2288.png)

### Advanced Security Analysis

![Example of advanced security analysis](https://user-images.githubusercontent.com/63926014/218797253-d5d01fed-e425-4379-9dfa-f29d862a82ec.png)

## Security Notes

- This tool is intended for educational purposes and authorized security testing only
- Always ensure you have permission to scan the target systems
- The OpenAI analysis provides general security information but should not replace professional security assessments
