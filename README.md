IndiaMART AI Content & Catalog Generator

    Purpose: Bypasses strict anti-bot captchas by handling the heavy lifting locally—taking a single product seed name, using Generative AI to craft descriptions, features, applications, and keywords, generating visuals, filling the PDF catalog template, and preparing the exact text fields for manual or semi-automated posting.

    Tech Stack: Python, Google Gemini API / OpenAI API, Pillow (PIL) / OpenCV for image processing, ReportLab (for PDF catalog generation).

    Key Features:

        AI Content Synthesis: Input a single product name to automatically generate 5 descriptive angles/image concepts, rich product descriptions, key features, industrial applications, and high-ranking search keywords.

        Catalog Auto-Assembly: Automatically drops product assets and names into a standardized master PDF template.

        Security Workaround: Explicitly documents how it solves the IndiaMART automation bottleneck—automating the asset generation and template preparation phases locally to streamline manual uploading when captchas block full browser automation.





I checked your repository:

[IndiaMART-AI-Content-Catalog-Generator](https://github.com/AbishekPranavGV/IndiaMART-AI-Content-Catalog-Generator?utm_source=chatgpt.com)

Right now, the main problem is that most of the actual project is stored only inside these ZIP files:

- `NUNES_INDIAMART_AUTOMATION_V5_3_SHARED_COMMON_PRO.zip`
- `NUNES_INDIAMART_PRODUCT_AUTOMATION_FAST_V3_EXACT_TEMPLATE.zip`

For a proper GitHub project, the real source code should be visible in folders rather than hidden inside ZIP archives.

I prepared a GitHub-ready restructuring package for you:

INDIAMART_AI_CONTENT_CATALOG_GITHUB_READY.zip[Download the GitHub-ready project package](sandbox:/mnt/data/INDIAMART_AI_CONTENT_CATALOG_GITHUB_READY.zip)

It contains the following project structure:

```text
IndiaMART-AI-Content-Catalog-Generator/
│
├── app/
├── data/
├── docs/
│   └── MIGRATION_GUIDE.md
├── scripts/
│   └── EXTRACT_EXISTING_PACKAGE.ps1
├── tests/
│
├── .env.example
├── .gitignore
├── requirements.txt
├── CHANGELOG.md
└── README.md
```

I also improved the project definition so it covers your actual IndiaMART workflow: product name/model, description, key features, applications, search keywords, product categories, **Specification / Additional Details**, product images, and PDF/mini-catalog generation.

### What you should do now

Download my ZIP and extract it. Then clone your repository:

```powershell
git clone https://github.com/AbishekPranavGV/IndiaMART-AI-Content-Catalog-Generator.git
cd IndiaMART-AI-Content-Catalog-Generator
```

Copy the files from my GitHub-ready folder into that repository.

Keep your two existing ZIP files there temporarily.

Then run:

```powershell
powershell -ExecutionPolicy Bypass -File .\scripts\EXTRACT_EXISTING_PACKAGE.ps1
```

That script will locate the latest existing IndiaMART package and extract it into:

```text
_extracted_source
```

Then we should identify the actual application files and move them into:

```text
app/
```

After that, push the cleaned structure:

```powershell
git add .
git commit -m "Restructure IndiaMART AI Content Catalog Generator project"
git push origin main
```

### Important

Do **not** delete your V5.3 ZIP yet. That should remain your known-working backup until the extracted source version runs correctly.

After testing, the final repository should roughly become:

```text
IndiaMART-AI-Content-Catalog-Generator
│
├── app
│   ├── main.py
│   ├── generator
│   ├── catalog
│   ├── image_processing
│   ├── templates
│   └── static
│
├── data
├── docs
├── scripts
├── tests
│
├── .env.example
├── .gitignore
├── requirements.txt
├── CHANGELOG.md
└── README.md
```

And your large working ZIP should eventually be placed under **GitHub Releases**, for example:

```text
IndiaMART AI Content & Catalog Generator v5.3
```

with:

```text
NUNES_INDIAMART_AUTOMATION_V5_3_SHARED_COMMON_PRO.zip
```

as the release download.

One limitation remains: the GitHub connection currently shows **read-only access (`push: false`)**, so I could inspect the repository but could not commit these files directly for you.
