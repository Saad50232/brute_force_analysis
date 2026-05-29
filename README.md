Brute Force Login Detection Analyzer
A Python-based log analysis tool that detects brute force SSH authentication attacks by parsing system logs, flagging suspicious IPs, and visualizing attack patterns — replicating the detection workflows used by Tier 1 SOC analysts.

What It Does

Parses raw auth.log files using regex to extract failed SSH login attempts
Counts failed attempts per source IP and flags repeat offenders above a threshold
Exports flagged IPs to suspicious_ips.txt as structured, actionable alerts
Visualizes attack frequency by IP and by hour of day using matplotlib


Why It Matters
Repeated failed logins from the same IP are the most common precursor to account takeovers. This tool automates the detection logic a SOC analyst would manually run during incident triage — identifying the pattern, surfacing the threat, and generating an output ready for escalation.

Tools & Technologies
ToolPurposePythonCore scripting and log parsingRegex (re)Pattern extraction from raw log filespandasData aggregation and IP frequency analysismatplotlibAttack visualization by IP and hour

How to Run
bash# Clone the repo
git clone https://github.com/Saad50232/brute-force-login-detector

# Install dependencies
pip install pandas matplotlib

# Add your auth.log file to the project directory

# Run the notebook
jupyter notebook brute_force_analysis.ipynb

Sample Output

Total failed login attempts detected: 6
Top flagged IP: 185.23.44.101 — 3 attempts in under 10 seconds
Suspicious IPs exported to suspicious_ips.txt for escalation
Bar charts showing attack volume by IP and by hour of day


Skills Demonstrated

Log analysis and parsing
Threshold-based threat detection
Incident triage and alert generation
SOC Tier 1 analyst workflows
Data visualization for security reporting


Author
Saad Chaudhry
CS Graduate — Rutgers University Newark | Splunk Fundamentals 1 Certified | CompTIA Security+ (In Progress)
LinkedIn | GitHub
