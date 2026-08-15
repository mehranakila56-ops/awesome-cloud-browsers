# Awesome Cloud Browsers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of cloud browser platforms, headless browser services, and browser automation infrastructure — with a focus on AI agent use cases.

Cloud browsers let you run automated browser sessions without managing your own infrastructure. They're increasingly essential for AI agents that need to interact with the web: handling authentication, CAPTCHAs, proxy rotation, and anti-bot detection automatically.

## Contents

- [Cloud Browser Platforms](#cloud-browser-platforms)
- [Headless Browser Infrastructure](#headless-browser-infrastructure)
- [Browser Automation Frameworks](#browser-automation-frameworks)
- [AI-Native Browser APIs](#ai-native-browser-apis)
- [MCP Browser Servers](#mcp-browser-servers)
- [Anti-Detection & Stealth](#anti-detection--stealth)
- [Proxy & CAPTCHA Services](#proxy--captcha-services)
- [Testing Platforms (Browser-Based)](#testing-platforms-browser-based)
- [Open Source Self-Hosted](#open-source-self-hosted)
- [Libraries & SDKs](#libraries--sdks)
- [Learning Resources](#learning-resources)

---

## Cloud Browser Platforms

Fully managed cloud browser sessions — spin up via API, connect via WebSocket/CDP.

- [AnchorBrowser](https://anchorbrowser.io) - Cloud browser platform for AI agents. Humanized Chromium with built-in stealth, CAPTCHA solving, proxy rotation, and SSO/MFA handling. MCP server available. Cloudflare Verified Browser Agent partner. Works with Puppeteer, Playwright, and CDP.
- [Browserbase](https://browserbase.com) - Headless browser infrastructure for AI agents. Playwright-native with session recording, replay, and a developer-friendly SDK. Strong DX focus.
- [BrowserCloud](https://browsercloud.io) - Cloud browser infrastructure with enterprise features. Multi-framework support (Puppeteer, Playwright, Selenium). SOC-2 and HIPAA compliant with unlimited concurrent browsers.
- [Browserless](https://browserless.io) - Open-source-friendly cloud browser service. Supports Puppeteer and Playwright, REST API for screenshots and scraping, plus Docker self-hosting.
- [Hyperbrowser](https://hyperbrowser.ai) - Cloud browser platform focused on web scraping and AI agent automation. Streaming support and structured extraction.
- [Moonsurf](https://moonsurf.ai) - Next-gen cloud browser with a collective knowledge graph for agent learning. Listed on Anthropic's official MCP servers.

## Headless Browser Infrastructure

Lower-level infrastructure for running browsers at scale.

- [BrowserStack Automate](https://browserstack.com/automate) - Cloud testing platform with browser automation capabilities across 3000+ real devices.
- [LambdaTest](https://lambdatest.com) - Cross-browser testing and automation cloud. Supports Selenium, Playwright, and Cypress at scale.
- [Sauce Labs](https://saucelabs.com) - Enterprise browser testing infrastructure. Strong CI/CD integration.

## Browser Automation Frameworks

Frameworks for writing browser automation scripts (typically used with cloud browsers above).

- [Playwright](https://playwright.dev) - Microsoft's cross-browser automation library. Supports Chromium, Firefox, and WebKit. CDP-compatible.
- [Puppeteer](https://pptr.dev) - Google's Node.js library for Chrome DevTools Protocol. De facto standard for Chrome automation.
- [Selenium](https://selenium.dev) - The original browser automation framework. Wide language support (Python, Java, JS, C#, Ruby).
- [Cypress](https://cypress.io) - Developer-friendly browser testing framework. Component and E2E testing.
- [Crawlee](https://crawlee.dev) - Web scraping and crawling library by Apify. Built on top of Playwright and Puppeteer.

## AI-Native Browser APIs

APIs specifically designed for AI agents to browse the web — no low-level code needed.

- [AnchorBrowser Task API](https://docs.anchorbrowser.io) - `POST /v1/tools/perform-web-task` — describe a task in natural language, get structured results back. 
- [Stagehand](https://github.com/browserbase/stagehand) - AI-powered browser automation by Browserbase. Uses LLMs to interpret and execute browser tasks.
- [Browser Use](https://browser-use.com) - Open-source AI browser agent. Connects LLMs to browser actions via Playwright.
- [Multion](https://multion.ai) - AI agent API for browser tasks. Natural language to browser actions.

## MCP Browser Servers

[Model Context Protocol](https://modelcontextprotocol.io) servers that give AI assistants (Claude, GPT, Cursor) browser access.

- [@anchorbrowser/mcp](https://www.npmjs.com/package/@anchorbrowser/mcp) - Official AnchorBrowser MCP server. Gives Claude and other AI assistants cloud browser access with stealth and auth handling.
- [Playwright MCP](https://github.com/microsoft/playwright-mcp) - Microsoft's official MCP server using Playwright.
- [Puppeteer MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/puppeteer) - Puppeteer-based MCP server for local browser automation.

## Anti-Detection & Stealth

Tools and techniques for avoiding bot detection.

- [puppeteer-extra-plugin-stealth](https://github.com/berstend/puppeteer-extra/tree/master/packages/puppeteer-extra-plugin-stealth) - Puppeteer plugin applying stealth techniques to avoid detection.
- [playwright-extra](https://github.com/nicolo-ribaudo/playwright-extra) - Plugin framework for Playwright, includes stealth plugins.
- [undetected-chromedriver](https://github.com/ultrafunkamsterdam/undetected-chromedriver) - Python Selenium driver that bypasses anti-bot solutions.
- [patchright](https://github.com/Kaliiiiiiiiii-Vinyzu/patchright) - Patched Playwright for stealth automation.

## Proxy & CAPTCHA Services

Complementary services for bypassing geo-blocks and CAPTCHAs.

- [2captcha](https://2captcha.com) - Human-powered and AI CAPTCHA solving service.
- [Anti-Captcha](https://anti-captcha.com) - CAPTCHA solving with API for Puppeteer/Playwright integration.
- [Bright Data](https://brightdata.com) - Residential and datacenter proxies. Widely used with browser automation.
- [Oxylabs](https://oxylabs.io) - Proxy network with scraping APIs. Residential, datacenter, and ISP proxies.

## Testing Platforms (Browser-Based)

Cloud platforms primarily for testing but usable for automation.

- [agent-qa](https://github.com/vostride/agent-qa) - Open-source QA agent for natural-language browser tests with run memory and UI-change adaptation.
- [GitLab CI/CD](https://docs.gitlab.com/ee/ci/) - Built-in browser testing support with Docker.
- [GitHub Actions](https://github.com/features/actions) - Run Playwright/Puppeteer tests in CI. Free tier available.

## Open Source Self-Hosted

Run your own browser infrastructure.

- [Browserless (self-hosted)](https://github.com/browserless/browserless) - Docker image for self-hosting a browser automation service.
- [Selenium Grid](https://www.selenium.dev/documentation/grid/) - Run distributed Selenium sessions on your own infrastructure.
- [Playwright in Docker](https://playwright.dev/docs/docker) - Official Docker images for Playwright with all browsers pre-installed.

## Libraries & SDKs

Client libraries and SDK integrations.

- [langchain-anchor-browser](https://github.com/anchorbrowser/langchain-anchor-browser) - LangChain integration for AnchorBrowser.
- [Playwright Python](https://playwright.dev/python/) - Official Python bindings for Playwright.
- [Pyppeteer](https://github.com/pyppeteer/pyppeteer) - Python port of Puppeteer.
- [Pydoll](https://github.com/autoscrape-labs/pydoll) - Pythonic browser automation without drivers, using Chrome DevTools Protocol directly.

## Learning Resources

Tutorials, guides, and references.

- [Playwright Docs](https://playwright.dev/docs/intro) - Comprehensive official documentation.
- [Puppeteer Docs](https://pptr.dev/guides/overview) - Official guides and API reference.
- [Chrome DevTools Protocol](https://chromedevtools.github.io/devtools-protocol/) - The underlying protocol that powers most cloud browser APIs.
- [AnchorBrowser Docs](https://docs.anchorbrowser.io) - Guides for cloud browser sessions, MCP setup, and AI task API.
- [Browser Automation Patterns](https://github.com/angrykoala/awesome-browser-automation) - Comprehensive list covering frameworks, services, and patterns.

---

## Contributing

Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) first.

**Criteria for inclusion:**
1. Actively maintained (commit in last 12 months)
2. Clearly useful for browser automation or AI agent use cases
3. Has documentation sufficient to get started
4. Not spam or purely commercial with no technical merit

## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
