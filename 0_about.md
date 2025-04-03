# County Emergency Rental Assistance Spending: An Introduction to the Project

## Background

The Federal Emergency Rental Assistance (ERA) program was administered by the U.S. Department of the Treasury to alleviate the impact of the COVID-19 pandemic on renter households.

A total of $46.55 billion was distributed to state, territorial, county, city, and tribal governments through two programs: ERA1 ($25.55 billion authorized in December 2020 as part of the Consolidated Appropriations Act of 2021) and ERA2 ($21 billion included with the American Rescue Plan Act, passed March 2021). States, Washington, D.C., and  territories were entitled to be ERA grantees. County and city governments were eligible to be ERA grantees if they met population requirements. Though Treasury set overall guidelines for the administration of the program, each grantee established its own mechanisms for the processing of applications and payments. Similarly, though Treasury published uniform data reporting requirements, each grantee had its own mechanisms for data collection and management.

Over the course of the two programs, ERA funds could be used to address various housing needs for low-income renters. For the purposes of this project we focus on assistance paid by grantees to address rent (forward and in arrears), utility costs (forward and in arrears), and 'other housing-related expenses' as defined by Treasury (such as relocation expenses). Assistance could be paid either to tenants, landlords, utility companies, or providers of housing-related expenses. Further details on eligibility requirements and programmatic guidance for ERA can be found on [Treasury's web site](https://home.treasury.gov/policy-issues/coronavirus/assistance-for-state-local-and-Tribal-governments/emergency-rental-assistance-program) for ERA.

This dataset details aggregate ERA spending at the county-month level and the county-total level. We attempted to establish broad coverage across the nation, aiming to share these data publicly with researchers interested in applying ERA payments data to their own research. 

This project was completed by a team comprising of the [Housing Initiative at Penn](https://www.housinginitiative.org/), the [Eviction Lab](https://evictionlab.org/) (Princeton University), and [Urban Deplacement Project](https://www.urbandisplacement.org/) (University of California, Berkeley), partially in fulfillment of an award from the U.S. Department of Housing and Urban Development. The project was also supported by grant R01NR020854 (MPI Eisenberg and Pollack). Hepburn's involvement is supported by R01NR020748.

The project team is solely responsible for the analytical decisions made in this project and the accuracy of aggregated files produced by this project. This work does not reflect the views of the U.S. Government or any other funding sources.

### Data Citation

The aggregate data produced by this project may be cited as:

Kim, Chi-Hyun, Grace Hartley, Jacob Haas, Tim Thomas, Rebecca Yae, and Peter Hepburn. County Emergency Rental Assistance Spending. 2025. Accessed via TKTK.

## Data sources

### PHPDFs

The main sources of data for this project were confidential ERA payment data reported to the U.S. Department of the Treasury by ERA grantees. ERA grantees were required to submit periodic, detailed reports to Treasury on the payments they had made for assistance to households. (However, Tribal grantees were exempt from the reporting payment-level data, and their payments are not reflected in this dataset. There were 301 Tribal grantees, with $841,390,378 in total allocations.) The reports to Treasury were intended to offer payment-by-payment details on how ERA funds were distributed, including: amounts and dates of payments, addresses of the assisted property, type of payment (e.g., rent arrearage), and type of payee (e.g., landlord). These reports were compiled by Treasury into large files called Participant Household Payment Data Files (PHPDFs), separately for ERA1 and ERA2. The project team received these data between August 2023 and May 2024.

For ERA1, Treasury compiled a closeout PHPDF based on the payments reported by grantees for the entirety of the ERA1 period of performance ending on December 29, 2022. This forms the basis of the ERA1 payments data used in this analysis.

For ERA2, the program was still within its period of performance through 2023. Grantees were required to submit data on a quarterly basis, reporting cumulative payments made from the beginning of ERA2 up to the end of the reporting period. We generally use the PHPDF for the 2023 Q4 reporting period, but supplement with data reported in earlier quarters in 2023 for grantees with good data quality in those files but with bad-quality or missing data in the Q4 file.

Whether the ultimate source of the assistance was ERA1 or ERA2 was largely immaterial for tenants and landlords, so our final aggregation does not distinguish between them. However, the two programs had slightly different administrative and reporting requirements, so for the purposes of our data processing pipeline, ERA1 and ERA2 are treated separately until just before the final aggregation.

Addresses in PHPDFs were primarily geocoded by HUD, except for a small percentage of records which failed HUD's geocoding. These records (77 records in ERA1 and 24,394 records in ERA2) were geocoded by the project team using the Census geocoder.

### Other data

We also made use of ancillary files, including:

- A crosswalk of grantees for ERA1 and ERA2 compiled by the National Low Income Housing Coalition
- Treasury's publicly released aggregate summary expenditure files ([ERA1](https://home.treasury.gov/system/files/136/Q1-2021-Q4-2022-ERA-Demographic-Data.xlsx), [ERA2](https://home.treasury.gov/system/files/136/ERA2-Cumulative-Program-Data-Q2-2021-Q3-2024.xlsx))
- Treasury's updated list of allocation amounts (including any reallocations made through June 2024)
- HUD's [ZIP code/county crosswalk](https://www.huduser.gov/portal/datasets/usps_crosswalk.html)
- A county/city population crosswalk generated from the [Geocorr engine](https://mcdc.missouri.edu/applications/geocorr.html)
  








