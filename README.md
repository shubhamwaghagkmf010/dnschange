{
  "tool_name": "DNSChange",
  "version": "1.0.0",
  "author": "Shubham Wagh",
  "exe_file": "DNSChange.exe",
  "description": "DNSChange is a portable Windows utility that allows you to instantly change your DNS server IPs using built-in netsh commands. Designed for one-click use, it's ideal for users who want a faster and safer internet experience.",
  "what_is_this": "DNSChange is a DNS configuration automation tool for Windows. Instead of changing DNS settings manually via Control Panel or network properties, it automates the process via a compiled .exe file that runs command-line instructions silently and effectively.",
  "why_it_exists": "This tool was created to save time, reduce user errors, and eliminate the need for complex manual DNS configuration. It ensures even non-technical users can update their DNS settings securely and quickly.",
  "why_use_this": [
    "Instant DNS configuration in one click",
    "Bypasses manual steps in Control Panel",
    "Increases browsing speed and privacy using reliable public DNS",
    "No need to open CMD or remember commands",
    "Lightweight and portable – no installation required"
  ],
  "how_to_use": [
    "1. Download the DNSChange.exe file from [Releases](https://github.com/shubhamwaghagkmf010/dnschange/releases/download/dnschange/DNSChange.exe).",
    "2. Right-click the file and select 'Run as Administrator'.",
    "3. Wait for the command to execute (CMD may briefly appear).",
    "4. DNS will be set automatically to the configured public IPs (Google DNS by default).",
    "5. You're done! DNS settings are now updated system-wide."
  ],
  "dns_applied": {
    "primary_dns": "8.8.8.8",
    "secondary_dns": "8.8.4.4"
  },
  "technology_used": [
    "Windows Command Line (CMD)",
    "netsh interface ip set dns",
    "Batch scripting compiled to executable (.exe)"
  ],
  "system_requirements": [
    "Operating System: Windows 10, 11, or later",
    "Permissions: Administrator rights required to change network settings"
  ],
  "tags": [
    "dns",
    "dns changer",
    "dns fixer",
    "netsh",
    "cmd tool",
    "networking",
    "batch to exe",
    "windows utility",
    "dns switcher",
    "internet speed",
    "google dns",
    "cloudflare dns"
  ],
  "repository": "https://github.com/shubhamwaghagkmf010/dnschange/releases/tag/dnschange",
  "license": "MIT",
  "created_with": "Custom Windows batch script compiled into an executable using a BAT-to-EXE compiler. Designed for simplicity and speed.",
  "upcoming_version": "The updated version with more features (including GUI support and enhanced DNS options) is coming soon. Stay tuned!"
}
