# What Killed Us, Then and Now

An interactive comparison of the ten leading causes of death in the United States in 1900 and 2024. Students make three guesses, then see both lists as bars on one scale, with each cause labeled as an infection, chronic disease, injury, or other. By Gwen Sharp, as a companion to Chapter 15 (Health and Illness) of *A Sociology Experiment*.

**Live site:** https://gsharpokie.github.io/causesofdeath/

## What it does

- **Three guesses:** the leading cause of death in 1900, life expectancy in 1900, and why cancer’s death rate is higher now.
- **Two top-ten lists** on a shared scale (deaths per 100,000 people), plus three summary numbers.
- **The fuller picture:** the shift from infections to chronic disease, the role of clean water and living conditions, why children gained the most, why heart disease and cancer rates look worse than they are, COVID-19, and causes sociologists study (suicide, overdoses).
- **Discussion questions.**

## For instructors

The lists stay hidden until the third guess. To open the page with them showing, add `#lists` to the link: https://gsharpokie.github.io/causesofdeath/#lists

## Data

- **1900:** National Center for Health Statistics, “Leading Causes of Death, 1900–1998.” Covers the death registration states (ten states and the District of Columbia). https://stacks.cdc.gov/view/cdc/53236
- **2024:** NCHS final mortality data: Xu, Murphy, Kochanek and Arias, “Mortality in the United States, 2024,” NCHS Data Brief No. 548 (January 2026), and NCHS FastStats “Deaths and Mortality.” The page calculates crude rates from the published numbers of deaths, the total (3,072,666), and the overall crude rate (903.4 per 100,000).
- **Life expectancy:** 47.3 years (1900) and 79.0 years (2024), NCHS.

## Updating it

NCHS publishes final data each winter. Open `index.html` on GitHub, select the pencil icon, and near the top of the `<script>` section edit `const Y2024 = {`: the overall rate (`all`), life expectancy (`life`), total deaths (`total`), and each cause’s number of deaths. The page calculates the rates. Also change the `2024` in the two places the year is shown (`col("col2024", 2024, Y2024)` and the “In ${2024}” sentence) and in the plain text of “The fuller picture” and “About the data.”

## Turning on the site (one time)

Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the **main** branch and the **/ (root)** folder, and select **Save**. Keep Issues turned on so the “Suggest a correction” link works.

## Author

Created by Gwen Sharp ([@gsharpokie](https://x.com/gsharpokie)).

## License

© 2026 Gwen Sharp. Licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): you may share and adapt it for noncommercial purposes with credit. See [LICENSE](LICENSE). The figures are from U.S. government sources; this license covers the page’s design, text, and code.
