# Assignment 1 - Option 2: Thanglish to Tamil (Playwright Project)

This repository contains Playwright automated tests for the Tamil transliteration tool at https://tamil.changathi.com/.

## Files included
- tests/example.spec.js  : Playwright test suite (replace selectors if necessary)
- ITPM_Assignment1_IT23555280.xlsx : Completed Excel with Positive, Negative and UI test cases

## How to run
1. Install Node.js (v16 or newer recommended).
2. In the `playwright_project` folder run:
   ```bash
   npm init -y
   npm i -D @playwright/test
   npx playwright install
   ```
   Or alternatively run the guided install:
   ```bash
   npm init playwright@latest
   ```
3. Run tests:
   ```bash
   npx playwright test
   ```

## Important notes
- The test script uses a generic selector `textarea` for the input/output. **Open the website (Right Click -> Inspect)** and replace `textarea` with the actual input and output selectors (for example `#InputText` and `#OutputText`) if they differ.
- The tests assume the tool updates the same textarea value with transliterated Tamil text. If the website uses two different elements (input & output), adjust the script to read from the output element (e.g., `await page.textContent('#output')` or `await page.inputValue('#output')`).
