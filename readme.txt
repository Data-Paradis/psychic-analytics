SCRIPTING LAYOUT

Data Extraction
    <root> folder
        <main.py> file (The code from other files are imported here, and the scripting to interact with the database is done here. This file collects the prompt word as an input, and does the entire scraping process and pushes to database)
        <twit_scraper.py> file (This file scrapes data from twitter based on the prompt given, and stores as a csv format)
        <other_scrapers.py> file(Same as twit_scraper, but for the particular website)
        CSV folder(All CSV files){temporary till we relocate to warehouse or lake}
        Readme.txt

#once done airflow should send mail to admins

Data Transformation and Analysis
    <root> folder
        <clean.py> file (The data is preprocessed, cleaned and easy analysis made)

#once done, a mail -containing the easy visualisations on the small, current data- should be sent to admins

Data Loading
    <root> folder
        <final_prep.py> file (data should be organised to be loaded in the particular format, to the particular database in the particular warehouse)
        <load.py> file (data loaded to a postgresql)


POSTGRESQL DB IS SHARED WITH DJANGO, DRF + CELERY + FRONT END TAKES OFF FROM THERE

Other Notes: Airflow should be used to automate the DAG workflow pipeline and singer can (by choice) assist with ETL

PS: THIS FRAMEWORK REMAINS DYNAMIC AND OPEN FOR ADJUSTMENTS


