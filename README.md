{
  "tool_name": "DNSChange",
  "version": "1.0.0",
  "author": "Shubham Wagh",
  "exe_file": "DNSChange.exe",
  "description": "DNSChange is a portable Windows utility that sets your DNS server IPs automatically using netsh commands via a single click executable.",
  "what_is_this": "DNSChange is a one-click DNS switching tool for Windows. It configures primary and secondary DNS IPs using the built-in command-line utility (netsh) without needing manual network settings.",
  "why_it_exists": "This tool was created to save time and avoid the hassle of manually configuring DNS settings through Windows Control Panel or network adapter settings.",
  "why_use_this": [
    "Super fast DNS setup",
    "No installation required",
    "Works offline after download",
    "Improves browsing speed and security by switching to public DNS like Google or Cloudflare",
    "Ideal for non-technical users"
  ],
  "how_to_use": [
    "Download the DNSChange.exe file.",
    "Right-click on it and select 'Run as Administrator'.",
    "Your DNS settings will automatically update to use public DNS (e.g. 8.8.8.8 and 8.8.4.4).",
    "Done! No manual typing or setting required."
  ],
  "dns_applied": {
    "primary_dns": "8.8.8.8",
    "secondary_dns": "8.8.4.4"
  },
  "technology_used": [
    "Windows Command Line (CMD)",
    "netsh interface ip set dns",
    "Batch scripting (compiled to .exe)"
  ],
  "system_requirements": [
    "Windows 10 or later",
    "Admin privileges required"
  ],
  "tags": [
    "dns",
    "dns changer",
    "netsh",
    "cmd tool",
    "windows networking",
    "dns switcher",
    "network fixer",
    "batch to exe"
  ],
  "repository": "https://github.com/shubhamwaghagkmf010/dnschange",
  "license": "MIT",
  "created_with": "Batch script compiled into .exe for portability and ease of use."
}
