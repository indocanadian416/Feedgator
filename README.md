# FeedGator 🐊

**Daily Cyber Threat Intelligence Aggregator**

A client-side cybersecurity threat intelligence dashboard that aggregates real-time threat feeds from multiple RSS/Atom sources. Designed for security professionals to monitor the latest cyber threats, vulnerabilities, and security news in one unified interface.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-web-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

## 🚀 Features

### Threat Intelligence
- **Automated threat tagging** with priority scoring (Ransomware, Zero-Day, CVE, Exploit, Malware, APT, etc.)
- **Intelligent prioritization** surfaces critical threats first using weighted scoring
- **25+ pre-configured feeds** from trusted cybersecurity sources
- **Real-time updates** with auto-refresh every 10 minutes

### Filtering & Analysis
- **Time-based scoping**: Today, Last 24h/48h/7 days, or All time
- **Keyword search**: Filter across titles, descriptions, and sources
- **Smart sorting**: By priority (cyber-critical first), newest, source, or title
- **Automatic deduplication** to avoid redundant articles

### Technical Capabilities
- **100% client-side** - no backend required, runs entirely in browser
- **Cross-platform** - works on any device with a modern browser
- **Privacy-focused** - all processing happens locally
- **Local caching** via localStorage for fast performance
- **Concurrent fetching** (12 parallel workers) for speed
- **TXT export** for filtered results (titles + links)

### User Experience
- **Dark/light mode** with automatic system preference detection
- **Progressive rendering** - displays results as feeds load
- **Responsive design** for desktop, tablet, and mobile
- **Accessibility** features with ARIA labels

## 📡 Pre-Configured Threat Feeds

FeedGator comes with 25+ trusted cybersecurity sources:

**News & Analysis**
- The Hacker's News
- Bleeping Computer
- Dark Reading
- Krebs on Security
- Security Week
- ZDNet Security
- CyberScoop
- SC Magazine
- Infosecurity Magazine
- Threatpost

**Government & Advisories**
- CISA Alerts
- SANS ISC
- US-CERT Alerts

**Vendor Threat Intelligence**
- Microsoft Security Blog
- Palo Alto Unit42
- Cisco Talos
- IBM Security Intelligence
- Kaspersky Securelist
- ESET WeLiveSecurity
- Sophos Naked Security
- Malwarebytes Blog
- Rapid7 Blog
- Qualys Blog

**Security Researchers**
- Bruce Schneier
- Graham Cluley

**Tech Platforms**
- Google Security Blog
- GitHub Security Blog

## 🛠️ Installation

### Option 1: GitHub Pages (Recommended)
Visit the live deployment: `https://indocanadian416.github.io/Feedgator/`

### Option 2: Local Deployment
```bash
# Clone the repository
git clone https://github.com/indocanadian416/Feedgator.git

# Navigate to directory
cd Feedgator

# Open index.html in your browser
open index.html
```

### Option 3: Web Server
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx http-server

# Then navigate to http://localhost:8000
```

## 📖 Usage

### Basic Operation
1. **Load Feeds**: Click "Load Feeds" to fetch from all configured sources
2. **Filter by Time**: Select scope (Today, 24h, 48h, 7d, All time)
3. **Search**: Use keyword filter to find specific threats or topics
4. **Sort**: Choose sorting method (Priority, Newest, Source, Title)
5. **Export**: Download filtered results as TXT file

### Adding Custom Feeds
1. Paste RSS/Atom feed URLs (one per line) in the text area
2. Click "Load Feeds" to fetch
3. Feeds are cached locally for quick reloads

### Keyboard Workflow
- Filters update automatically on change
- Use search to quickly find CVEs, threat actors, or specific vulnerabilities
- Export function respects current filters and scope

## 🏷️ Threat Tag Categories

FeedGator automatically tags and prioritizes articles:

**Critical Priority (Red)**
- Ransomware
- Zero-Day
- CVE
- Exploit
- Breach
- Backdoor

**High Priority (Yellow)**
- Malware
- APT
- DDoS
- Supply Chain
- IoC (Indicators of Compromise)

**Medium Priority (Blue)**
- Phishing
- Patch
- Cloud
- Identity
- Network
- Web Vulnerabilities
- Email Threats

**Low Priority**
- Crypto/Blockchain

## 🔧 Configuration

### Adjustable Parameters (in code)
```javascript
const MAX_ITEMS_PER_FEED = 400;      // Articles to fetch per feed
const AUTO_REFRESH_MINUTES = 10;     // Auto-refresh interval
const CONCURRENCY = 12;              // Parallel fetch workers
const REQUEST_TIMEOUT_MS = 12000;    // Per-feed timeout
```

### Cache Management
- Cache stored in `localStorage` under key `feedgator_cache_v6`
- Click "Clear Cache" to force fresh fetch
- Cache includes feed URLs, articles, and timestamps

## 🎯 Use Cases

### Threat Hunting
- Monitor emerging threats and CVEs
- Track ransomware campaigns and threat actors
- Identify zero-day vulnerabilities in your stack

### Incident Response
- Quick access to latest security advisories
- Real-time vendor patch notifications
- IOC discovery and threat correlation

### Security Operations
- Daily threat landscape awareness
- Executive briefing preparation
- Security awareness content curation

### Research & Learning
- Stay current on security trends
- Follow specific threat actors or campaigns
- Discover new attack techniques and TTPs

## 🔒 Security & Privacy

- **No telemetry**: Zero tracking or analytics
- **Client-side only**: No data sent to external servers (except RSS sources)
- **CORS proxy**: Uses AllOrigins API to bypass CORS restrictions
- **Local storage**: All caching happens in your browser
- **No authentication**: No accounts or login required

## 🌐 Browser Compatibility

- Chrome/Edge (Chromium) 90+
- Firefox 88+
- Safari 14+
- Opera 76+

**Note**: Requires modern browser with JavaScript enabled and localStorage support.

## 📱 Responsive Design

- **Desktop**: 3-column grid layout
- **Tablet**: 2-column grid layout
- **Mobile**: Single column with optimized touch targets

## 🤝 Contributing

Contributions welcome! Areas for improvement:
- Additional RSS feed sources
- Enhanced tagging logic
- Performance optimizations
- UI/UX improvements
- Export format options (JSON, CSV)

## 📝 License

MIT License - free for personal and commercial use.

## 👤 Author

**Pratik Goswami**
- GitHub: [@indocanadian416](https://github.com/indocanadian416)
- Role: Threat Researcher & Hunter

## 🙏 Acknowledgments

- All cybersecurity news sources and threat intelligence providers
- [AllOrigins](https://allorigins.win/) for CORS proxy service
- Security community for RSS feed recommendations

## 📊 Statistics

- **Feeds**: 25+ pre-configured sources
- **Coverage**: Global cybersecurity news and threat intel
- **Update Frequency**: Auto-refresh every 10 minutes
- **Fetch Speed**: 12 concurrent workers
- **Max Items**: 400 per feed (10,000+ total potential articles)

---

**Built with ❤️ for the cybersecurity community**

*Stay informed. Stay secure. Hunt threats efficiently.*