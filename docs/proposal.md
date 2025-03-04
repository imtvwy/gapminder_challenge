# Project Proposal

## Motivation and Purpose

Our Role: Educational NGO

Target Audience: Students, General Public Interested in Development

This project is designed to augment the gapminder [worldview upgrader](https://upgrader.gapminder.org/) tool that MDS students were introduced to at the beginning of the program. [Gapminder](https://www.gapminder.org/) is an NGO founded to address systematic misconceptions about global development. Gapminder provides free-to-access data and teaching material on global development based on reliable statistics. Their worldview upgrader involves participants answering questions about various topics linked to [UN development goals](https://sdgs.un.org/goals), and being provided correct answers with accompanying explanations. This project proposes to augment the experience of the worldview upgrader by providing interactive visualizations along with answers to questions related to UN development goals, leveraging the [Gapminder dataset](https://cran.r-project.org/web/packages/gapminder/README.html). This allows users to explore and manipulate the data supporting the answers to the questions, allowing for a dynamic and enriched learning experience.

## Description of the Data

The [dataset](https://raw.githubusercontent.com/UBC-MDS/gapminder_challenge/main/data/raw/world-data-gapminder_raw.csv) we will be using for visualization contains approximately 39,000 rows of summarized data from the [Gapminder dataset](https://www.gapminder.org/data/). Gapminder combines data from multiple sources and the complete Gapminder dataset contains hunderds of indicators. The dataset we will be using is a summary dataset which contains 14 columns with demographic indicators from 1800 to 2018. The visualization app will mainly focus on the recent data, for example from 1900 onwards, for relevancy.

Each data row can be uniquely identified by `country` and `year`. `country` is associated with `region` and `sub_region` which will be useful for filtering within the visualizations. Other possible filters can be built will be `population` and `income group` (High, Upper Middle, Low Middle, Low), depending on the context of the plot.

The demographic indicators we will be using in this visualization app are `children_per_woman`(total fertility rate), `life_expectancy` (in years), `child_mortality` (under age five) and `income`. All of these indicators are numeric variables containing no or very few missing values.  A new variable `income per capita` will be derived from `income` and `population` for fair comparison of income across countries and over time.

## Research Questions and Usage Scenarios

### Audience Persona and Usage Example

Lisa is an incoming first year political science student at UBC. She is passionate about global development and knows that she has a lot to learn. Excited for her program, she is searching for information online about the subject. Like many other users of the dashboard, she is in the “unknown unknowns” phase of understanding of global development. That is to say, she does not know where the gaps in her knowledge lie about our world’s complex society. The dashboard offers her a chance to explore her preconceptions about developed and developing countries in an interactive and visual setting.

For example, she navigates to the part of the dashboard relating to childbirth. With respect to the amount of children that women have, Lisa predicts that the average number worldwide is around 4. In seeing the answer to the question, she realizes that her views would have been correct in the 1990s but are not consistent with today’s reality of closer to 2.75. By adjusting the year slider, she sees that average childbirth numbers were relatively stable from the 1800s onwards until about 1960, after which there is a rather steep drop. She is intrigued by this experience and she decides to learn more by exploring other questions in the interactive dashboard and Gapminder’s [worldview upgrader](https://upgrader.gapminder.org/).
