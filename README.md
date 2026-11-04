# Healthcare Operations & Financial Intelligence Dashboard

## Project Overview

The **Healthcare Operations & Financial Intelligence Dashboard** is an
Excel-based data analytics project that examines hospital encounter
activity, service patterns, claim costs, payer coverage, and encounter
duration.

The project uses healthcare encounter data and related reference tables
to provide an aggregated view of operational and financial performance.
The dashboard is designed to help hospital management explore service
utilization and recorded financial activity.

All analysis is performed in Microsoft Excel using structured tables,
formulas, PivotTables, PivotCharts, and slicers.

## Project Objectives

The project aims to:

-   Measure total encounter activity and the number of unique patients
    represented in the encounter records.
-   Examine how encounter volumes change from year to year.
-   Identify the most common encounter classes and descriptions.
-   Compare total and average claim costs across encounter classes and
    payers.
-   Review recorded payer coverage against total claim costs.
-   Examine the distribution of encounter durations.

## Dataset Overview

The workbook includes the following source tables:

  -----------------------------------------------------------------------
  Table / Worksheet                   Description
  ----------------------------------- -----------------------------------
  `encounters`                        Encounter-level records, including
                                      start and stop timestamps, patient,
                                      organization and payer references,
                                      encounter class, claim cost and
                                      payer coverage.

  `patients`                          Patient reference information. This
                                      sheet contains personally
                                      identifying fields and must not be
                                      included in a public copy.

  `organizations`                     Organization reference information.

  `payers`                            Payer reference information.

  `procedures`                        Procedure-level records associated
                                      with encounters.

  `data_dictionary`                   Descriptions of the source tables
                                      and their fields.
  -----------------------------------------------------------------------

The encounter table contains **27,891 records** and represents **974
distinct patient IDs**. The recorded encounter period runs from **2
January 2011 to 5 February 2022**.

## Dashboard Contents

The dashboard presents the following indicators and visual analyses:

### Key Performance Indicators

-   **Total Encounters:** 27,891 encounter records.
-   **Unique Patients:** 974 distinct patient IDs represented in the
    encounter table.
-   **Total Claim Cost:** \$101,514,375.52.
-   **Average Claim Cost:** \$3,639.68 per encounter.
-   **Recorded Payer Coverage:** \$31,097,506.99, equivalent to
    approximately 30.63% of total claim cost.

### Visual Analysis

The dashboard includes:

1.  **Yearly Encounter Trend** -- compares encounter volumes across
    calendar years.
2.  **Total and Average Claim Cost by Encounter Class** -- compares the
    financial contribution and average claim cost of each encounter
    class.
3.  **Total and Average Claim Cost by Payer** -- compares encounter
    volume and average claim cost across payer categories.
4.  **Duration Band** -- shows how encounters are distributed across the
    duration categories created in the workbook.
5.  **Total Cost by Encounter Description** -- highlights the
    descriptions associated with the recorded claim costs.

PivotTables supporting the dashboard are organised on the `Sheet1`
worksheet, while the visual dashboard is presented on `Sheet4`.

## Key Findings

The workbook's current PivotTable results show:

-   Ambulatory encounters account for the largest encounter class by
    volume, with **12,537 encounters**.
-   Ambulatory encounters also have the highest total claim cost, at
    approximately **\$36.28 million**.
-   Inpatient encounters have the highest average claim cost among the
    encounter classes, at approximately **\$7,761.35**.
-   Recorded payer coverage totals approximately **\$31.10 million**, or
    **30.63%** of total claim cost.
-   The encounter records span 2011 to early 2022. The 2022 data is
    incomplete and should not be compared directly with full calendar
    years.

These findings describe the recorded data; they do not, on their own,
explain the causes of cost differences or establish actual payments
received.

## Tools and Excel Features

-   Microsoft Excel
-   Excel Tables
-   Structured references and calculated columns
-   Excel formulas for encounter duration and duration bands
-   PivotTables and PivotCharts
-   Slicers and report connections
-   Data validation and independent calculation checks

## Validation and Data Quality

The following checks were used or should be retained as part of the
final validation evidence:

-   Confirm the encounter count against the number of records in the
    encounter table.
-   Confirm the unique patient count using distinct patient IDs rather
    than counting encounter rows.
-   Independently sum `TOTAL_CLAIM_COST` and `PAYER_COVERAGE` from the
    encounter-level data.
-   Recalculate average claim cost as total claim cost divided by the
    number of encounters.
-   Apply dashboard filters and confirm that connected PivotTables and
    KPIs respond as expected.
-   Check that clearing filters restores the overall totals.
-   Review missing values, duplicate encounter IDs, date fields and
    calculated duration values.

The current source data contains 27,891 encounter records, 974 distinct
patient IDs and no duplicate encounter IDs. The total claim cost and
payer coverage totals are \$101,514,375.52 and \$31,097,506.99
respectively.

## Assumptions and Limitations

-   Each row in the `encounters` table is treated as one encounter.
-   Unique patients are counted using distinct patient IDs in the
    encounter table.
-   Average claim cost is calculated as total claim cost divided by the
    number of encounter records.
-   Recorded payer coverage is interpreted as the coverage amount
    recorded in the dataset. It is not assumed to equal cash received or
    final reimbursement.
-   A zero payer coverage value does not necessarily mean that no
    payment was made; it may reflect the way coverage was recorded.
-   The 2022 records cover only part of the year, through 5 February
    2022.
-   The workbook contains one organization in the organization reference
    data. Therefore, organization-level comparisons cannot be
    meaningfully interpreted with this dataset.
-   Duration analysis depends on the quality and consistency of the
    start and stop timestamps. Unusually long calculated durations
    should be investigated before drawing operational conclusions.
-   The analysis is descriptive. It does not establish clinical quality,
    patient outcomes, reasons for cost differences or causal
    relationships.

## Business Recommendations

1.  **Review high-cost encounter categories.** Investigate the service
    and resource factors contributing to the high total cost of
    ambulatory encounters and the high average cost of inpatient
    encounters. Additional clinical and resource-use context is required
    before attributing causes.

2.  **Strengthen payer coverage monitoring.** Review encounters with
    zero or low recorded payer coverage and reconcile the dataset with
    payment and reimbursement records. Recorded coverage alone does not
    establish the amount ultimately collected.

3.  **Use encounter trends to support capacity planning.** Monitor
    annual changes in encounter volumes and compare them with staffing,
    equipment and service capacity. The incomplete 2022 period should be
    treated separately.

4.  **Improve duration data quality.** Review unusually long encounter
    durations and verify start and stop timestamps before using duration
    results to make operational decisions.

## Privacy and Responsible Use

**Patient confidentiality is a mandatory requirement for this project.**

The original workbook contains patient names, addresses and patient
identifiers in its source worksheets. It must not be uploaded to a
public repository or shared publicly in its current form.

Before publishing or sharing a version of this project:

-   Remove the `patients` worksheet and any unnecessary patient-level
    source data.
-   Remove or anonymize patient IDs and any fields that could identify
    an individual.
-   Check PivotTables, PivotChart source ranges, hidden worksheets,
    formulas, comments, file properties and screenshots for identifying
    information.
-   Share only aggregated results that do not reveal individual patient
    records.
-   Keep the original source workbook in a private, access-controlled
    location.

Do not include patient names, addresses, patient IDs, or other
unnecessary identifying information in public reports, screenshots,
dashboards or repositories.

## Project Files

The main working file is the Excel workbook:

`Healthcare Operations & Financial Intelligence Dashboard.xlsx`

The workbook contains the source worksheets, supporting PivotTables and
dashboard charts. A separate sanitized public copy should be created
before publishing.

## Conclusion

This project demonstrates how Microsoft Excel can be used to transform
healthcare encounter data into an interactive operational and financial
dashboard. It provides an overview of encounter activity, encounter
categories, claim costs, payer coverage and duration patterns while
documenting the assumptions, limitations and privacy requirements
relevant to interpreting and sharing the results.
