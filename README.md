# What Killed Us, Then and Now

An interactive comparison of the ten leading causes of death in the United States in 1900 and 2024. Students make three guesses, then see both lists as bars on one scale, with each cause labeled as an infection, chronic disease, injury, or other. By Gwen Sharp.

**Live site:** https://gsharpokie.github.io/causesofdeath/

## What it does

- **Three guesses:** the leading cause of death in 1900, life expectancy in 1900, and why cancer’s death rate is higher now.
- **Two top-ten lists** on a shared scale (deaths per 100,000 people), plus three summary numbers.
- **Follow a cause over time:** three line charts with a year slider, lines that can be turned on and off, and a table of the numbers. “Today’s leading causes” (heart disease, cancer, stroke, accidents; age-adjusted, 1900–2024), “Infections that faded” (tuberculosis, pneumonia and flu, diarrhea; crude rates, 1900–1953), and “Flu and COVID-19” (age-adjusted, 1900–2023). For any year, the page shows each cause’s rate and how it compares with the first year on the chart.
- **The fuller picture:** the shift from infections to chronic disease, the role of clean water and living conditions, why children gained the most, why heart disease and cancer rates look worse than they are, COVID-19, and causes sociologists study (suicide, overdoses).
- **Discussion questions.**

## For instructors

The lists stay hidden until the third guess. To open the page with them showing, add `#lists` to the link: https://gsharpokie.github.io/causesofdeath/#lists

To jump straight to the charts, add `#trends` instead: https://gsharpokie.github.io/causesofdeath/#trends

## Data

- **1900:** National Center for Health Statistics, “Leading Causes of Death, 1900–1998.” Covers the death registration states (ten states and the District of Columbia). https://stacks.cdc.gov/view/cdc/53236
- **2024:** NCHS final mortality data: Xu, Murphy, Kochanek and Arias, “Mortality in the United States, 2024,” NCHS Data Brief No. 548 (January 2026), and NCHS FastStats “Deaths and Mortality.” The page calculates crude rates from the published numbers of deaths, the total (3,072,666), and the overall crude rate (903.4 per 100,000).
- **Life expectancy:** 47.3 years (1900) and 79.0 years (2024), NCHS.
- **Charts, age-adjusted rates:** 1900–2018 from the National Center for Health Statistics dataset “Age-adjusted Death Rates for Selected Major Causes of Death” (https://data.cdc.gov/d/6rkc-nb2q). 2019–2024 from the “Data table for Figure 4” in each year’s “Mortality in the United States” data brief (Nos. 395, 427, 456, 492, 521, and 548). The 2018 figures in the dataset match Data Brief 395. Flu and pneumonia ends in 2020 and COVID-19 covers 2020–2023 because the briefs list only the ten leading causes.
- **Charts, crude rates:** tuberculosis (1900–1953), diarrhea and enteritis (1900–1931), and pneumonia and influenza (1900–1953) from “Leading Causes of Death, 1900–1998,” for the years each was among the ten leading causes.

## Updating it

NCHS publishes final data each winter. Open `index.html` on GitHub, select the pencil icon, and near the top of the `<script>` section edit `const Y2024 = {`: the overall rate (`all`), life expectancy (`life`), total deaths (`total`), and each cause’s number of deaths. The page calculates the rates. Also change the `2024` in the two places the year is shown (`col("col2024", 2024, Y2024)` and the “In ${2024}” sentence) and in the plain text of “The fuller picture” and “About the data.”

**Charts:** the chart numbers are in the second `<script>` block, between `DATA:START` and `DATA:END`, as `year:rate` pairs. Each winter, add the new year’s age-adjusted rates for heart disease, cancer, stroke, and accidents from the new data brief’s “Data table for Figure 4.”

## Turning on the site (one time)

Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the **main** branch and the **/ (root)** folder, and select **Save**. Keep Issues turned on so the “Suggest a correction” link works.

## Accessibility

This site aims to meet [WCAG 2.1](https://www.w3.org/TR/WCAG21/) Level AA, so it works for people who use screen readers, keyboards, or screen magnification.

- All buttons, sliders, and links can be reached and used with a keyboard, and show a visible outline when selected.
- Charts have text descriptions, and many also have a data table or a slider that reads out each value.
- Text meets WCAG AA color contrast standards.
- Pages fit narrow phone screens without sideways scrolling.

I checked it in November 2026 with automated accessibility testing (axe-core) plus keyboard and small-screen checks. It hasn’t yet been tested by people who use screen readers every day, so there may be problems I haven’t caught. If something doesn’t work for you, please [let me know](https://github.com/gsharpokie/causesofdeath/issues/new).

## Author

Created by Gwen Sharp ([@gsharpokie](https://x.com/gsharpokie)).

## License

© 2026 Gwen Sharp. Licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): you may share and adapt it for noncommercial purposes with credit. See [LICENSE](LICENSE). The figures are from U.S. government sources; this license covers the page’s design, text, and code.
