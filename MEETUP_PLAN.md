# MCP Intro Meetup Plan — Guizhou University Study Group

Planning document for next month's study-group session: an introduction to the Model Context Protocol (MCP). Audience: ~10 students with laptops. Format: short intro video, plain-language explainer, recent-news context, then optional deeper-dive tutorial and hands-on time.

---

## 1. What is MCP? (Overview)

The **Model Context Protocol (MCP)** is an open-source standard for connecting AI applications to external systems — data sources (local files, databases), tools (search engines, APIs), and services — so that AI apps like Claude or ChatGPT can reach the context and capabilities they need.

The most common analogy: **MCP is like "USB-C for AI."** Just as USB-C provides a standardized way to connect electronic devices, MCP provides a standardized way to connect AI applications to external systems. Instead of building a custom integration between every AI app and every tool (an N×M integration problem), each side implements the protocol once: an AI application acts as an **MCP client**, and each data source or tool exposes an **MCP server**. Any compatible app can then use any compatible tool without custom integration code.

- Introduced by Anthropic in November 2024 and open-sourced; now supported across a wide range of clients and servers (IDEs, coding platforms like Replit and Sourcegraph, and more).
- MCP servers expose **tools, resources, and prompts** through one consistent interface.
- Practical examples: an agent reading your Google Calendar and Notion; Claude Code generating a web app from a Figma design; enterprise chatbots querying multiple databases.

**Official documentation:** https://modelcontextprotocol.io

(Reference: "What is the Model Context Protocol (MCP)?" — modelcontextprotocol.io; Anthropic's "Introducing the Model Context Protocol" announcement, anthropic.com; Wikipedia "Model Context Protocol".)

---

## 2. Recent News / Announcements (openers for the session)

- **"Software to software workflows: mean.md offers starter kit as MCP passes 10,000 servers"** — openPR (Oct 19, 2026). The open standard for connecting AI agents to tools and data has passed 10,000 published servers; a builder guide now offers a starter kit. Great scale-of-ecosystem stat to open the session with.
  https://openpr.com/news/4666542/software-to-software-workflows-mean-md-offers-starter-kit-as

- **"Radware Introduces Model Context Protocol (MCP) Server Protection to Help Secure the Integration Layer of Agentic AI"** — Markets Insider (Oct 14, 2026). A purpose-built security product for MCP as AI agents gain deeper access to enterprise apps, data, and workflows — good segue into the security discussion.
  https://markets.businessinsider.com/news/stocks/radware-introduces-model-context-protocol-mcp-server-protection-to-help-secure-the-integration-layer-of-agentic-ai-1036624834

*(Also worth having in your back pocket: Ars Technica, "MCP for agent-to-agent comms may be the riskiest protocol you've never heard of" — https://arstechnica.com/security/2026/10/vulnerability-in-agents-from-google-and-others-exposes-structural-flaw-in-mcp — if the group wants to dig into trust-model concerns.)*

---

## 3. Videos

### Short intro video (screen at the start of the session)

- **"Model Context Protocol (MCP) Explained in 90 Seconds"** — YouTube, 1:51. A quick explainer of what MCP is and why it's the missing link for deploying AI agents.
  https://www.youtube.com/watch?v=mMWWU4PambM&vl=en

### Longer hands-on / tutorial video (for people who want to go deeper)

- **"MCP Tutorial: Build Your First MCP Server and Client from Scratch (Free Labs)"** — YouTube, 40:14. Full walkthrough of how AI agents book flights, check databases, or interact with websites via MCP, including building a server and client from scratch with free labs.
  https://www.youtube.com/watch?v=RhTiAOGwbYE

*(Backup options: "How Model Context Protocol (MCP) actually works" — https://www.youtube.com/watch?v=cGuyrANVi4A (7:58); "Build your first MCP Server: Tutorial for Beginners" — https://www.youtube.com/watch?v=egVm_z1nnnQ (37:00).)*

---

## 4. Venue Shortlist (Guiyang — quiet spots for ~10 people with laptops, a couple of hours)

All three candidates are in the city center around Wenchang Road / Yan'an Road (Nanming & Yunyan districts), convenient for people coming from the Guizhou University area.

1. **Starbucks Coffee (Hengte City Plaza / 亨特城市广场)**
   - Address: 1F, Hengte City Plaza (亨特城市广场1层), 18 Jichang Rd (机场路18号), Wenchang S Rd area, Nanming District, Guiyang, Guizhou 550003
   - Website: https://starbucks.com.cn/
   - Chain café in a large mall — reliable Wi-Fi, plenty of tables and power outlets, and the mall setting makes it easy to reconfigure seating for a group of ~10.

2. **12 Weidu Cafe**
   - Address: 23F, Business Building of Guiyang Hotel (贵阳饭店商务楼23层), 2 Yan'an E Rd (延安东路2号), Yunyan District, Guiyang, Guizhou 550003
   - Telephone: +86 851 8586 6191
   - Independent café on a high floor of the Guiyang Hotel's business building — quieter than street level, good for a study group; call ahead to reserve a corner for ~10.

3. **Reading Time Cafe**
   - Address: HPG9+XR2, Wenchang S Rd, Nanming District, Guiyang, Guizhou 550003
   - Small café near the other candidates; the "reading" theme suggests a quieter, laptop-friendly atmosphere — drop by or call to confirm they can seat 10 together for a couple of hours.

*Note: the venue search did not return ratings or opening hours for these candidates, so please verify hours and seat availability by phone/visit before announcing. 12 Weidu Cafe is the only one with a listed phone number so far (+86 851 8586 6191).*

---

## 5. Suggested Session Flow (for discussion)

1. Welcome + intros (5 min)
2. Screen the 90-second MCP intro video (2 min)
3. Plain-language explainer with the USB-C analogy + architecture (client/servers, tools/resources/prompts) (15 min)
4. News round-up: 10,000+ servers milestone; security angle (5–10 min)
5. Q&A / discussion (10 min)
6. Optional deep-dive: start the 40-minute build-your-own-server tutorial for those who want to go further
