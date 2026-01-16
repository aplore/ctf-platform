<p align="center">
  <img src="https://img.shields.io/badge/Platform-CTF-%23FF6B00?style=for-the-badge&logo=linux" alt="Platform">
  <img src="https://img.shields.io/badge/License-APLORE_CTF-%23e6005c?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/Status-LIVE_CTFs-%2334A853?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Players-500+-blue?style=for-the-badge" alt="Players">
</p>

<h1 align="center">
  <br>
  <img src="https://raw.githubusercontent.com/aplore/ctf-platform/main/.github/ctf-logo.png" alt="APLORE CTF Platform" width="220">
  <br>
  APLORE CTF WARZONE
  <br>
</h1>

<h3 align="center">⚔️ The Official Capture The Flag Platform for Aplore Cyber Guardians ⚔️</h3>
<h4 align="center">Professional-grade cybersecurity challenges • Real-world attack simulations • Live Scoreboards</h4>

<p align="center">
  <a href="#-blood-red-rules">Rules</a> •
  <a href="#-ctf-arenas">Arenas</a> •
  <a href="#-flag-submission">Submission</a> •
  <a href="#-leaderboard-system">Leaderboard</a> •
  <a href="#-ethical-framework">Ethics</a> •
  <a href="#-getting-started">Start</a>
</p>

![CTF Dashboard](https://raw.githubusercontent.com/aplore/ctf-platform/main/.github/dashboard-preview.png)

## 🩸 BLOOD RED RULES

### **GOLDEN RULE: RESPECT THE BATTLEGROUND**
> This is a controlled warzone for education. What happens here, stays here.

1.  **NO REAL-WORLD ATTACKS**: Challenges are isolated to `*.ctf.aplore.tech` domains and provided Docker containers.
2.  **NO BRUTE FORCE** against the platform infrastructure (rate limits apply).
3.  **NO SHARING SOLUTIONS** publicly during active competitions. Post in private writeup channels only.
4.  **REPORT VULNERABILITIES** in the platform itself via `security@aplore.tech` for bounty.
5.  **ONE ACCOUNT PER PLAYER**. Multi-accounting results in permanent ban.

**Violation = Immediate disqualification + possible removal from Aplore programs.**

## 🏆 CTF ARENAS

### **🔥 WEEKLY WARFARE (Every Saturday 00:00 UTC - 23:59 UTC)**
| Arena | Difficulty | Category | Flags | Points |
|-------|------------|----------|-------|--------|
| **Web Penetration** | Beginner → Expert | Web Security | 8-12 | 1000-5000 |
| **Binary Reversing** | Intermediate → Advanced | Reverse Engineering | 4-6 | 2000-8000 |
| **Network Cryptography** | Mixed | Crypto/Networking | 6-8 | 1500-6000 |
| **Forensic Investigation** | Beginner → Advanced | Digital Forensics | 5-7 | 1200-4500 |

### **⚡ MONTHLY SIEGE (Last Weekend Monthly)**
- **48-Hour Marathon CTF**
- **Team-based (3-5 members)**
- **Progressive difficulty scaling**
- **Real-world inspired scenarios**
- **Prize pool for top 3 teams**

### **🎓 APLORE CURRICULUM CTFs**
- **Course-aligned challenges**
- **Unlimited attempts**
- **No time limits**
- **Educational focus with hints**

## 🚩 FLAG SUBMISSION

### **Flag Format**
All flags follow this pattern unless otherwise specified:
```bash
APLORE{...}  # Case-sensitive, includes curly braces
Submission Methods
bash
# 1. Web Interface (Primary)
https://ctf.aplore.tech/challenges

# 2. CLI Tool (For power users)
curl -X POST https://api.ctf.aplore.tech/submit \
  -H "X-API-Key: YOUR_TOKEN" \
  -d '{"challenge_id": "web-101", "flag": "APLORE{...}"}'

# 3. Discord Bot (Quick submissions)
!submit web-101 APLORE{...}
🏅 LEADERBOARD SYSTEM
Scoring Algorithm
python
def calculate_score(base_points, solves, time_bonus, first_blood=True):
    """
    Dynamic scoring system:
    - Base points decrease with more solves
    - Time bonus for early submissions
    - 2x multiplier for first blood
    """
    return (base_points * (1/solves**0.5)) + time_bonus * (2 if first_blood else 1)
Ranking Categories
Badge	Requirement	Privileges
🥇 CYBER LEGEND	Top 10 All-Time	Platform admin access, challenge creation rights
🥈 WARRIOR ELITE	Top 25 Monthly	Early challenge access, private mentoring
🥉 GUARDIAN	Top 50 Weekly	Priority support, custom badge
🔰 INITIATE	First flag captured	Basic writeup access
⚖️ ETHICAL FRAMEWORK
Challenge Philosophy
"We simulate attacks to teach defense. Every vulnerability you exploit here represents one you'll learn to patch in the real world."

Responsible Practice
Isolated Environments: All challenges run in Docker/Sandbox

No Malware: Challenges contain no real malware

Safe Exploitation: Techniques are contained within challenge scope

Knowledge Transfer: Skills must be used only on authorized systems

Prohibited Techniques
DDoS/DoS attacks against platform

Social engineering of other players

Automated scanning beyond challenge scope

Sharing exploit chains publicly before CTF ends

🚀 GETTING STARTED
Step 1: Registration
bash
# Register on platform
https://ctf.aplore.tech/register

# Or use CLI
ctf-cli register --email student@aplore.com --username your_handle
Step 2: Team Formation
bash
# Create team (Monthly Siege only)
ctf-cli team create "Team_Name" --members "user1,user2,user3"

# Join existing team
ctf-cli team join "Team_Name" --invite-code CODE123
Step 3: First Challenge
bash
# List beginner challenges
ctf-cli challenges list --difficulty beginner

# Get challenge details
ctf-cli challenge view web-101

# Submit first flag
ctf-cli flag submit web-101 "APLORE{w3lc0m3_t0_th3_w4rz0n3}"
Step 4: Writeup Submission
markdown
# Template for writeups
Challenge: web-101
Difficulty: Beginner
Time spent: 2 hours
Methodology:
1. Reconnaissance with gobuster
2. Found /admin panel
3. SQL injection in login
4. Boolean-based extraction
5. Found flag in users table

Tools used: gobuster, sqlmap, burpsuite
Learning points: SQLi basics, directory busting

Flag: APLORE{sql1_b4s1cs_m45t3r3d}
🛡️ PLATFORM SECURITY
For Players
End-to-end encrypted communications

No personal data stored in challenges

Anonymous participation option

Regular security audits

For Infrastructure
All challenges containerized

Network isolation between challenges

Resource limiting per player

Automated backup and monitoring

📞 SUPPORT & COMMUNITY
Live Support Channels
Platform	Channel	Purpose	Response Time
Discord	#ctf-warzone	General help, team finding	< 30 min
Discord	#ctf-writeups	Solution discussions (post-competition)	< 2 hours
Telegram	@aplore_ctf_bot	Automated notifications, submissions	Instant
Email	ctf-support@aplore.tech	Technical issues, platform bugs	< 24 hours
Mentor Assistance
bash
# Request mentor help (for stuck challenges)
!mentor request web-101 "Stuck at SQL injection after finding admin panel"

# Available 24/7 during competitions
# Mentors provide hints, not solutions
Upcoming Competition Schedule
text
JAN 2024: Web Application Siege (Jan 27-28)
FEB 2024: Binary Exploitation Marathon (Feb 24-25)
MAR 2024: Network Security Grand Prix (Mar 30-31)
APR 2024: Aplore Annual Championship (Apr 27-28) - $10,000 Prize Pool
🏆 HALL OF FAME
Current Season Leaders
yaml
Season-2024-Q1:
  First Place: "Ghost_in_the_Shell" - 48,500 points
  Second Place: "Zero_Cool" - 42,300 points  
  Third Place: "Acid_Burn" - 39,800 points
  Most First Bloods: "Crash_Override" - 17 first bloods
  Best Writeups: "Lord_Nikon" - 25 detailed writeups
All-Time Legends
Phantom Protocol (2023 Champion) - Now Aplore Security Instructor

Cipher_Queen (2022 Champion) - Lead Pentester at TechCorp

Binary_Bandit (2021 Champion) - Vulnerability Researcher

🔧 TECHNICAL SPECIFICATIONS
Platform Stack
yaml
Frontend: React.js + Tailwind CSS
Backend: Node.js + Express
Database: PostgreSQL + Redis
Containers: Docker + Kubernetes
Scoring Engine: Custom Python microservice
Monitoring: Prometheus + Grafana
Challenge Development
bash
# Challenge template structure
ctf-platform/
├── challenges/
│   ├── web/
│   │   ├── web-101/
│   │   │   ├── docker-compose.yml
│   │   │   ├── README.md
│   │   │   ├── src/
│   │   │   └── solution.md
│   ├── crypto/
│   ├── reversing/
│   └── forensic/

# Submit your own challenge
ctf-cli challenge submit --category web --difficulty medium --files ./my-challenge/
📜 LICENSE & LEGAL
Competition License
text
APLORE CTF PLATFORM LICENSE v2.0
- Challenges intellectual property belongs to creators
- Writeups become CC-BY-NC 4.0 after competition ends
- Platform code is proprietary to Aplore
- Player data is protected under our Privacy Policy
Legal Compliance
🇰🇪 Compliant with Kenya's Computer Misuse Act

🇺🇸 Aligned with US CFAA guidelines for educational use

🇪🇺 GDPR compliant for EU participants

🔒 Regular third-party security audits

<p align="center"> <strong>THE BATTLEGROUND AWAITS. YOUR SKILLS WILL BE TESTED. YOUR METTLE WILL BE PROVEN.</strong> <br> <code>ACCESS CODE: APLORE{ENTER_THE_WARZONE}</code> <br> <sub>© 2024 APLORE CTF PLATFORM | Training Africa's Cybersecurity Elite</sub> </p><p align="center"> <a href="https://ctf.aplore.tech">ENTER WARZONE</a> • <a href="https://discord.gg/tPe8fqXFN">JOIN DISCORD</a> • <a href="https://github.com/aplore/cybersecurity-roadmap">VIEW CURRICULUM</a> </p> ```
