## Clinimetric SAS Macros Documentation

All SAS macros exists to save time and development! These are a mix of procedures like macros, utilities and functions that are useful during production of SDTM/ADaM data sets and TFL creation.

### Getting Started

#### Macro Properties

- filenames much match macro names
- filenames must be lowercase, without spaces
- macro names must be lowercase
- macro prefixes:
  - _gm_ stands for General macros as procedures
  - _gu_ stands for General utilities
  - _sm_ stands for SDTM macros as procedures
  - _su_ stands for SDTM utilities
  - _am_ stands for ADAM macros as procedures
  - _au_ stands for ADAM utilities
  - _rm_ stands for Reporting (TFL) macros as procedures
  - _ru_ stands for Reporting (TFL) utilities 

### Reporting Macros

### rmreport.sas reference

Generates RTF report

***PARAMETERS:***

| Parameter        | Type     | Default   | Details                                                                                                           |
|------------------|----------|-----------|-------------------------------------------------------------------------------------------------------------------|
| data             | Optional | _LAST_    |  SAS data set                                                                                                     |
| columns          | Required |           | Describes the arrangement of all columns and of headings that span more than one column.                          |
| formats          | Optional |           | Assigns a SAS or user-defined format to the item. This format applies to report-item as PROC REPORT displays it.  |
| lengths          | Optional |           | Sets the cell width. Uses `BESTw.` for numeric variables and `$w.` for character variables.                       |
| labels           | Optional |           | Assigns descriptive labels to variables.                                                                          |
| ordervars        | Optional |           | Variables will be arranged in the specified order.                                                                |
| noprintvars      | Optional |           | Variables to suppresses the display of the report item.                                                           |
| linevars         | Optional |           | Specify the variable to display as categories.                                                                    |
| boldlinevars     | Optional |           | Bold the `LINEVARS=` varaibles.                                                                                   |
| linebreakafter   | Optional |           | Inserts a blank line after `LINEVARS=` varaibles.                                                                 |
| linebreakbefore  | Optional |           | Inserts a blank line before `LINEVARS=` varaibles.                                                                |
| centrealign      | Optional |           | Align variable values to centre.                                                                                  |
| leftalign        | Optional |           | Align variable values to left.                                                                                    |
| rightalign       | Optional |           | Align variable values to right.                                                                                   |
| decimalalign     | Optional |           | Specify the variables to have decimal alignment. All decimal alignment are done from right direction.             |
| decimalpadding   | Optional | 0         | Numeric value to move the aligned decimal values toward left direction.                                           |
| indentvars       | Optional |           | Specify the variables to have leading indentation for all values.                                                 |
| indentsubsetvar  | Optional |           | Specify the variables to have leading indentation for subset of values.                                           |
| indentsubsetcond | Optional |           | Conditional logic for `INDENTSUBSETVAR=` without `if/where` keys.                                                 |
| indentspace      | Optional | 2         | Integer value to apply as space. `Default=2` denotes four character space.                                        |
| orientation      | Optional | LANDSCAPE | Page orientation. Either LANDSCAPE or PORTRAIT.                                                                   |
| pgbreakobs       | Optional |           | Integer value to apply page break in PROC REPORT display.                                                         |
| fileid           | Required |           | Filename without extension to save the RTF report.                                                                |

***EXAMPLES:***


### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
