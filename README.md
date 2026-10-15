# Awesome-AI-Privacy-Watermark-Removal

## Top AI Privacy & Watermark Removal Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Provenance Metadata Stripping, Invisible Watermark Neutralization & Content Privacy*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **AI Privacy & Watermark Removal**. These tools enable content owners to strip provenance metadata, neutralize invisible watermarks, and sanitize AI-generated content—removing C2PA manifests, EXIF tags, and statistical watermarks from files they own.



**Examples** include Truepic, Reality Defender, Sensity AI, Optic, GetReal Security, Attestiv, C2PA Verify, Hive AI, Adobe Content Authenticity, and DeepMedia (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, metadata scrubbing, and open watermark neutralization—ideal for privacy engineers, content creators, and developers seeking transparent, vendor-independent provenance management.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms

| Platform | Description | Pricing | Free Tier Limit |
| :--- | :--- | :--- | :--- |
| **[Truepic](https://truepic.com/)** | Content authenticity and provenance platform built on C2PA standards. Vision capture verification & C2PA signing. | Starting at **$1,000/month** for entry deployment (~$15.00–$50.00/virtual inspection tier) | Free demo available upon request; no perpetual free plan |
| **[Reality Defender](https://www.realitydefender.com/)** | Enterprise deepfake & AI detection across image, video, audio, and text with explainable results and API. | Starting at **$399/month** (RealScan Business plan, billed annually) | **50 scans/month** free forever on developer tier |
| **[Sensity AI](https://sensity.ai/)** | Deepfake detection, visual threat intelligence, face manipulation analysis, and KYC liveness verification. | Starting at **$29/month** (Premium tier with ~50 analyses) | **3 analyses/month** free forever on starter tier |
| **[Optic](https://optic.ai/)** | AI content detection and provenance platform (AI or Not / Optic ID engine). | Starting at **$5/month** (Pro plan with $10 monthly detection credits; pay-as-you-go from $0.02/image) | **$5 in one-time free credits** (~250 free image checks) on signup |
| **[GetReal Security](https://getrealsecurity.com/)** | Media forensics & deepfake detection for enterprise identity and communications defense. | Custom enterprise contract starting at **~$15,000/year** ($1,250/month equivalent) | 14-day guided proof-of-concept trial (capped at 500 scans) |
| **[Attestiv](https://attestiv.com/)** | Digital media authentication, tamper detection, and media forensics for insurance and enterprise. | Custom business tier starting at **$500/month** (base API integration package) | 14-day free trial (up to 100 validation queries) |
| **[C2PA Verify](https://contentcredentials.org/verify)** | Adobe's reference web tool for Content Credentials & C2PA manifest verification. | **100% Free** (public reference utility by CAI / C2PA) | **Unlimited** free web manifest inspections |
| **[Hive AI](https://thehive.ai/)** | Multimodal AI content moderation, deepfake detection, and generative AI identification APIs. | Pay-as-you-go starting at **$6.00 per 1,000 image/deepfake checks** ($1.50/1k OCR; $10/audio hr) | **$50 one-time free promotional API credits** upon registration and payment method verification |
| **[Adobe Content Authenticity](https://contentauthenticity.adobe.com/)** | Content Credentials signing, verification, and generative AI disclosure ecosystem. | Included with Adobe Creative Cloud plans (starting at **$9.99/month**) or standalone free web tool | **Free perpetual access** for web-based C2PA inspection and basic credential signing |
| **[DeepMedia](https://deepmedia.ai/)** | AI-powered media forensics, multimodal deepfake detection, and DeepID provenance intelligence. | Enterprise API plans starting at **$750/month** (usage-based credit tiers) | 14-day enterprise trial (up to 200 media forensics API calls) |



## Open-Source GitHub Projects



- **[watermarks-remover](https://github.com/guillaumemeyer/watermarks-remover)**  

  **The most comprehensive open-source AI privacy utility for provenance marks and metadata** (MIT). **19,000+ GitHub stars** within weeks of launch—one of the fastest-growing privacy tools of 2026 . **Developed by French developer Guillaume Meyer** in response to Anthropic's announcement of invisible watermarks in Claude outputs . **Three-layer architecture**: **Layer A** (deterministic cleaning) removes hidden Unicode characters, zero-width joiners, bidi overrides, and tag characters from text; **Layer B** (statistical watermark disruption) rewrites text via external models to break token-sampling patterns—covering Claude, Gemini/SynthID-Text, OpenAI, and open LLM Kirchenbauer-style watermarks ; **File layer** strips C2PA/EXIF/XMP metadata from PNG, JPEG, WebP, SVG, PDF, DOCX, ODT, HTML, and Markdown . **Pure Python 3.10+ standard library**—near-zero installation cost. **Ollama and OpenAI-compatible model support** for local rewriting . **Honest about limits**: "在厂商放出公开检测器和密钥之前，没有任何工具能诚实证明'通过了官方检测失败'" —no tool can honestly claim detection failure until vendors release public detectors .



- **[universal-ai-watermark-remover](https://pypi.org/project/universal-ai-watermark-remover/)**  

  **Universal deep learning AI watermark remover and provenance metadata scrubber** (PyPI). **The most feature-complete open-source image watermark removal toolkit.** Features **LaMA neural inpainting** for visible watermark removal—synthesizes authentic textures (sky, clouds, fur) with zero smudging . **Complete C2PA and provenance metadata scrubbing**—scans raw binary byte streams for `c2pa` and `jumb` chunks, strips cryptographic provenance manifests (DALL-E 3, Adobe Firefly, ChatGPT) verified on contentcredentials.org/verify . **AI text and document steganography sanitizer**—detects and strips invisible Unicode watermarks (zero-width spaces, joiners, BOM, bidi overrides, tag characters) from Markdown, Plain Text, DOCX, ODT, and HTML . **Interactive side-by-side web studio** with adjustable brush masking and 1-click auto mask . **Invisible watermark neutralization** (SynthID) via FFT sub-band filtering . **Full video inpainting pipeline** with audio pass-through .



- **[remove-ai-watermarks](https://github.com/wiltodelta/remove-ai-watermarks)**  

  **CLI and Python library to strip visible and invisible AI watermarks and provenance metadata** (MIT). **The most accessible open-source image watermark remover.** Features **visible watermark removal** (Gemini sparkle, vendor text marks), **invisible watermark removal** through diffusion regeneration, **C2PA/EXIF/XMP/IPTC metadata stripping**, and **region-specific erasing** with coordinates . **Multiple removal backends**: OpenCV inpainting, **MI-GAN**, **LaMA**, and **qwen-zimage** (highest fidelity for face-heavy images, CUDA only) . **Online version at raiw.cc** for users who don't want to install Python . **Verified against provider verifiers** for specific output files—"That result applies to these files, not to every seed, image, or future watermark version" .



- **[watermark-remover](https://pypi.org/project/watermark-remover/0.4.0/)**  

  **Tools for finding and removing AI provenance signals from files you own** (PyPI). **The most text-focused open-source watermark removal toolkit.** **Layer A** removes zero-width characters, space-swaps, and other reversible Unicode artifacts . **Layer B** replaces original wording via LLM rewrite to disrupt statistical watermarks—with explicit warning: "重写会扁平化语气与精度" (rewriting flattens voice and precision) . **Character-level perturbations** (zero-width, space-swap, confusable, case) inspired by 2026 character-perturbation research—explicitly "not a hygiene pass and carries no detector guarantee" . **Image visible mark removal** with MorphoMod and external detector/inpainter adapters . **Opt-in image degradation** (frequency-domain DCT, blur, median, jpeg, rotate) for invisible watermark disruption .



- **[SynthID Watermark Remover](https://huggingface.co/spaces/Clock070303/synth-id-remover)**  

  **Research tool demonstrating removal of invisible SynthID watermarks from AI-generated images** (MIT). **The most transparent open-source SynthID removal implementation.** Based on the **SynthID-Bypass research** by 00quebec . **Three-step technique**: Canny edge detection for structural extraction, **low-denoise diffusion** (multiple passes at 0.05-0.3 strength) to "re-noise" the image and replace watermark-carrying pixels, and **ControlNet guidance** to preserve composition and structure . **Explicitly educational and AI safety research only**—"Do NOT use for malicious purposes, Do NOT use to circumvent copyright, Do NOT use to misrepresent content origin" . **Honest about technique**: "watermarks embedded in pixel space are vulnerable to reconstruction-style attacks" .



- **[c2pa (Go)](https://github.com/richardwooding/c2pa)**  

  **Pure Go implementation of C2PA validation** (MIT). **The most standards-compliant open-source C2PA verifier.** Performs the **complete C2PA validation algorithm** in pure Go—COSE signature verification (ES256/384/512, PS256/384/512, EdDSA), certificate chain and C2PA profile enforcement, hash bindings (hard binding and assertion hashed_uri), **Merkle BMFF verification** for fragmented assets, **RFC 3161 timestamp** full CMS signature verification, revocation (OCSP/CRL, opt-in), and **CAWG identity assertions** . **Structured validation results** with per-step status codes and explanations . **No network access required**—offline verification by default .



- **[c2patxt](https://pypi.org/project/c2patxt/)**  

  **Text watermarking using C2PA standards** (PyPI). **The most sophisticated open-source text provenance implementation.** Embeds marks as **variation selectors** costing 3 or 4 UTF-8 bytes per manifest byte . **Survives copy-paste** where applications preserve variation selectors . **Does NOT survive NFC/NFD normalization**—canonically equivalent forms that render identically can still invalidate the binding ("assertion.dataHash.malformed") . **Explicitly documents limits**: "Detects every stored-byte edit? No. The binding covers NFC-normalized text" . **Generation uses Ed25519**; validation accepts the full C2PA 2.4 signature set . **No quantum resistance**—all accepted algorithms are classical .



- **[encypher-c2pa](https://pypi.org/project/encypher-c2pa/)**  

  **Local-first, verification-only C2PA + CAWG SDK for Rust, Python, Go, and browser JavaScript** (PyPI). **The most privacy-preserving open-source C2PA verifier.** **Verification stays local by default and makes no network call** . **Packaged trust snapshots** with caller-supplied PEM bundle extension . **Explicit separation of conclusions**: integrity, signature, hard_binding, trust, revocation, freshness are all reported independently . **`--no-default-trust`** ignores packaged lists and evaluates only caller-supplied material . **Optional Encypher API cross-check** sends only asset SHA-256, byte length, MIME type, and bounded verdict summary—never the full asset .



- **[c2pa-rs](https://github.com/encypherai/c2pa-rs)**  

  **Rust library for C2PA and CAWG identity assertions** (MIT/Apache-2.0). **The reference open-source C2PA implementation.** Creates and signs C2PA claims and manifests, creates/signs/validates **CAWG identity assertions**, embeds manifests in supported formats, parses and validates manifests . **Thread-safe Context API** for configuration (Send + Sync, multiple instances) . **Supports C2PA v2 claims by default** .



- **[jpegtrust](https://pypi.org/project/jpegtrust/)**  

  **Embed, extract, and verify JPEG Trust provenance metadata** (PyPI). **The most accessible open-source C2PA embedding toolkit.** Based on C2PA and JUMBF standards . **Trust profiles** define verification rules as YAML expressions—**newsroom, insurance, creator, and ai-labelling templates** included . **Batch operations** for directories . **Verification reports** with pass/warning/fail status and scores .



- **[magicdispel](https://pypi.org/project/magicdispel/)**  

  **Privacy-focused metadata stripper that rebuilds files from allowlist** (PyPI). **The most surgical open-source metadata cleaner.** **Rebuilds a new file from an allowlist**—keeps only image data and fields needed to display it (color, orientation, HDR, ICC profile), writes some afresh . **Verifies the result**: must parse on its own, decode to identical frames, satisfy ExifTool . **Refuses files that cannot be safely rebuilt** (damaged, RAW, unknown structures) instead of passing them through . **Preserves HDR gain maps and color profiles**—unlike `exiftool -all=` which strips them and shifts colors . **Detailed format support table** showing exactly what is kept and removed per format .



- **[image-provenance-inspector](https://pypi.org/project/image-provenance-inspector/)**  

  **Open-source tool for inspecting image metadata, C2PA Content Credentials, and editing provenance** (PyPI). **The most honest open-source provenance inspector.** **Does not collapse uncertain origin and editing signals into one overconfident label** . **Two independent dimensions**: `origin` (CAMERA_CAPTURED, SYNTHETIC, UNKNOWN) and `editing` (NONE_DETECTED, TRADITIONAL, GENERATIVE, UNKNOWN) . **Camera metadata reported as medium-confidence evidence, not proof**—"provenance can be stripped, lost during export, or incomplete" . **Optional original-versus-edited comparison** using SSIM, perceptual hash, and difference mask . **REST API with Pydantic-validated JSON contract** .



- **[pagedmark](https://pypi.org/project/pagedmark/)**  

  **Visible and invisible watermark removal with 8GB Mac support** (PyPI). **The most resource-conscious open-source image watermark remover.** **Streams weights from CPU one module at a time**—peak device memory 0.28 GiB on 8GB Mac vs 7.70 GiB resident on 16GB Mac, at 24.1s vs 7.1s wall time . **Refuses devices that cannot run invisible removal** instead of falling back to something that will not finish . **Preview mode** capped at 512px for quick fidelity assessment . **Honest about trade-offs**: a 1.52 GiB saving was "measured, implemented, and then withdrawn" because it caused black rectangles over faces . **Metal numerical floors** documented and pinned by tests—below face strength 0.05, fp16 produces garbage .



- **[bonafide](https://pypi.org/project/bonafide/)**  

  **Calibrated, provenance-first framework for detecting AI-generated media** (PyPI). **The most epistemically honest open-source AI detector.** **Treats detection as evidence aggregation under uncertainty**—fuses hard provenance (C2PA), watermarks (SynthID), and ML detectors into one calibrated probability with confidence interval . **Abstains when evidence doesn't support a confident call** . **C2PA-signed image gives real explained verdict**: "100% AI-generated (CI 99-100%), basis=digitalSourceType:trainedAlgorithmicMedia, validation_state=Trusted, signer=Adobe Inc." . **Unsigned images, spoofs, and ordinary text all return abstain** .



### Additional Strong Open-Source Options



- **[proofof-ai-mcp](https://pypi.org/project/proofof-ai-mcp/)** — Digital content verification MCP server (MIT) . Detects AI-generated text, checks images for deepfake signatures, generates signed content certificates, verifies provenance via C2PA/Content Credentials .

- **[deepfake-detector-mcp](https://pypi.org/project/deepfake-detector-mcp/)** — Deepfake detection MCP server (MIT) . Analyzes images, videos, and audio for manipulation artifacts, checks metadata and provenance chains .

- **[Image Metadata Remover (Apify)](https://apify.com/andrew_babo/ai-footprint-remover)** — Bulk image metadata remover (Apify actor) . Removes EXIF, GPS, IPTC, XMP, ICC, Stable Diffusion prompt chunks, C2PA Content Credentials, and AI-generated labels . **Lossless by default**—pixels bit-identical, mean delta 0 . **Scrub mode** for classic invisible watermarks (DWT-DCT) .

- Community **n8n** workflows for provenance scanning and metadata cleaning automation.



**Frameworks for building custom systems**: Combine **watermarks-remover** for text provenance stripping with **universal-ai-watermark-remover** for image watermark removal, **magicdispel** for surgical metadata cleaning, **c2pa-rs** or **c2pa (Go)** for standards-compliant provenance verification, and **bonafide** for calibrated AI detection—creating a fully self-hosted, privacy-preserving provenance management stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- **AI watermark and provenance removal tools are for lawful use on content you own.** Removing AI labels and disguising content as human-made may violate copyright law, platform terms of service, and regulations including **EU AI Act Article 50** (AI content disclosure, effective August 2026) . **Use these tools responsibly.**

- **Open-source provenance tools are mature for metadata stripping, emerging for watermark neutralization.** `magicdispel` provides surgical metadata cleaning with allowlist-based rebuilding . `watermarks-remover` handles C2PA/EXIF/XMP across text and documents . `universal-ai-watermark-remover` handles visible watermarks with LaMA inpainting . **Invisible watermark removal (SynthID) is non-deterministic**—the SynthID-Bypass research demonstrates that pixel-space watermarks are vulnerable to reconstruction attacks, but no tool can guarantee detection failure without vendor-released detectors .

- **C2PA is the provenance standard, and open-source implementations are complete.** `c2pa-rs` provides the reference Rust implementation . `c2pa (Go)` provides full pure-Go validation . `c2patxt` handles text provenance with variation-selector encoding . **These are standards-compliant and production-grade.**

- **Honesty about limits is a feature, not a bug.** `watermarks-remover` states: "在厂商放出公开检测器和密钥之前，没有任何工具能诚实证明'通过了官方检测失败'" . `bonafide` abstains when evidence is insufficient . `image-provenance-inspector` reports origin as UNKNOWN when evidence is absent . **Tools that claim guaranteed removal are lying.**

- **Metadata stripping is lossy by design.** `magicdispel` preserves HDR gain maps and color profiles—unlike `exiftool -all=` which strips them and shifts colors . **Not all metadata removal is equivalent.** The Apify actor's "lossless" mode keeps pixels bit-identical while removing metadata containers .

- Self-hosted open-source solutions require proper security hardening and ongoing maintenance. **Provenance data is cryptographically bound to file bytes**—stripping manifests invalidates signatures and removes the provenance chain outright .



---



**Made for privacy engineers, content creators, and developers building transparent provenance management solutions.**  

Let's make AI Privacy & Watermark Removal more open, data-driven, and honest about limits.
