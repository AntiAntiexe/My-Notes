# Extract, transform, load

Extract, transform, load (ETL) is a three-phase process where data is extracted from and input source, transformed, and finally loaded into and output data container.

# Extract

- The ETL process involves extracting the data from the sources system(s). This regarded as one of the most important stages in ETL since extracting data correctly sets the stage for the success of subsequent processes.
- Each separate system may also use data from different data organization and/or format.
- Common data-source formats include relational databases, flat-file databases, XML, and JSON, but may also include non-relational database structures such as IBM Information Management System or other data structures such as Virtual Storage Access Method (VSAM) or Indexed Sequential Access Method (ISAM), or even formats fetched from outside sources by means such as a web crawler or data scraping.
- This part also involves data validation to confirm whether the data pulled from the sources has the correct/expected values in a given domain (such as a pattern/default or list of values).
- If the data fails the validation rules, it is rejected entirely or in part.
- The rejected data is ideally reported back to the source system for further analysis and to rectify incorrect records or preform data wrangling.

# Transform

- A series of rules or functions are applied to the extracted data in order to prepare it for loading into the end target.
- An important function is data cleansing. Which:
    - aims to pass only “proper” data to the target.
- Here is a list of some different transformation types that may be required to meet the business and technical needs of the server or data warehouse:
    - Selecting only certain columns to load: (or selecting null columns not to load). For example, if the source data has three columns (aka "attributes"), roll_no, age, and salary, then the selection may take only roll_no and salary. Or, the selection mechanism may ignore all those records where salary is not present (salary = null).
    - Translating coded values: (e.g. if the source system codes male as 1 and female as 2, but the warehouse codes male as M and female as F).
    - Encoding free form values (mapping Male to M)
    - Deriving a new calculate value: (e.g. sale_amount = qty*unit_price)
    - Sorting or ordering the data based on a list of columns to improve search performance.
    - Joining data from multiple sources (e.g. lookup, merge) and de duplicating the data.
    - Aggregating (e.g. summarizing multiple rows of data, total sales for each store, and for each region etc)
    - Transposing or pivoting (turning multiple columns into multiple rows or vice versa).
    - Splitting a column into multiple columns
    - Applying any form of data validation; failed validation may result in a full rejection of the data, partial rejection, or no rejection at all, and thus none, some, or all of the data is handed over to the next step depending on the rule design and exception handling; many of the above transformations may result in exceptions, e.g., when a code translation parses an unknown code in the extracted data.

# Load

- The load phase loads the data into the end target, which can be any data including a simple delimited flat file or a data warehouse.
- Depending on the requirements of the organization this process varies widely.