<script>
  import "highcharts/modules/exporting";
  import ArticleTextCloser from "../lib/ArticleTextCloser.svelte";
  import Footnote from "../lib/Footnote.svelte";
</script>

<div>
  <section>
    <article></article>
    <h1>Citations:</h1>
    <Footnote>
      <ul>
        <li>
          The Black Wealth Data Center. (2025). Explore Data - Employment.
          “Median Annual Earnings for Full-Time Workers (25-34 Years Old) by
          Race/Ethnicity (Nationwide, 2010-2022)”. Blackwealthdata.org.
          https://blackwealthdata.org/explore/employment
        </li>
        <li>
          The Black Wealth Data Center. (2025). Explore Data - Employment.
          “Median Income by Race/Ethnicity (County-wide, 2023)”.
          Blackwealthdata.org. https://blackwealthdata.org/explore/employment
        </li>
        <li>
          The Black Wealth Data Center. (2025). Explore Data - Employment.
          “Health Insurance Coverage by Race/Ethnicity (County-wide, 2023)”.
          Blackwealthdata.org. https://blackwealthdata.org/explore/employment
        </li>
        <li>
          The Black Wealth Data Center. (2025). Explore Data - Population.
          “Population Counts by Race/Ethnicity (County-wide, 2023)”.
          Blackwealthdata.org. https://blackwealthdata.org/explore/population
        </li>
        <li>
          The Black Wealth Data Center. (2025). Explore Data - Employment.
          “Primary Care Health Professional Shortage Areas (County-wide, 2024)”.
          Blackwealthdata.org. https://blackwealthdata.org/explore/employment
        </li>
        <li>
          2021 National Healthcare Quality and Disparities Report [Internet].
          Rockville (MD): Agency for Healthcare Research and Quality (US); 2021
          Dec. ACCESS TO HEALTHCARE AND DISPARITIES IN ACCESS. Available from:
          https://www.ncbi.nlm.nih.gov/books/NBK578537/
        </li>
        <li>
          Awan, Omer. “How Income Can Affect Your Health and Population
          Health.” Forbes, 4 June 2025,
          www.forbes.com/sites/omerawan/2025/06/04/how-income-can-affect-your-health-and-population-health/
        </li>
      </ul>
    </Footnote>
  </section>
</div>

<style>
  div {
    background-color: #e6e6e6;
    display: flex;
    flex-direction: column;
  }
  section {
    display: flex;
    height: 50vh;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
  h1 {
    font-family: 'DM Serif Display';
  }
</style>
