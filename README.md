# RC 저역통과 진폭비 계산기

커패시터 양단 출력의 이상 RC 저역통과 진폭비 계산

- Plan ID: E087
- App: https://nanalab.kr/eng-rc-lowpass-gain/
- Repository: https://github.com/NaNaCompany/eng-rc-lowpass-gain
- Formula: `|H| = 1/√(1+(2πfRC)²)`
- Output: 전압 진폭비 |H|

## Model

R,C>0, f≥0. 이상 전원·직렬 R과 접지 C·커패시터 양단 무부하 출력을 가정한다. 위상·복소응답·실제 소자 기생성분은 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `0.84673301596483`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
