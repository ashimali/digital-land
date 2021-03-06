---
title: "Step 1: Create your .csv files"
---

{{% contents %}}
- [Publish your developer contributions data]({{< ref "_index.md" >}})
- Step 1: Create your .csv files
- [Step 2: Update your developer contributions web page]({{< ref "update-your-developer-contributions-web-page.md" >}})
- [Step 3: Update the national register of developer contributions]({{< ref "update-the-national-register-of-developer-contributions.md" >}})
{{% /contents %}}

{{% inset-text %}}
To complete step 1 you must be able to create or amend .csv files, for example by using spreadsheet software.
{{% /inset-text %}}

If you are a planning authority using third-party software to manage your developer contributions, ask your vendor if the software can export the data to .csv files as defined in this guidance. Otherwise, use the following instructions.

Developer contributions data must be entered in 3 separate .csv files. A .csv file (or comma separated value file) is a universally recognised file format for storing tabular data in plain text. Storing the data in 3 separate files rather than one file reduces duplication and makes the data easier to use and maintain.

We’ve created a .csv template for each of the 3 files:

* [developer agreements](/guidance/developer-contributions/developer-agreement_YYYYMMDD.csv)
* [developer agreement contributions](/guidance/developer-contributions/developer-agreement-contribution_YYYYMMDD.csv)
* [developer agreement transactions](/guidance/developer-contributions/developer-agreement-transaction_YYYYMMDD.csv)

If it helps, you can use the above example files and enter your developer contributions data. You must follow the guidelines below, then 'save as .csv file'. You can use software such as Microsoft Excel, Google Sheets or Apple Numbers, as long as they meet the requirements of this guidance.

Each of the .csv files must:

* be named using the convention specified in each section below
* contain certain column headers (written exactly as shown, in lowercase)
* include 1 row of data for each agreement, contribution or transaction (as relevant)
* only entries that conform to the constraints described below

For general information on creating a .csv file see the W3C’s [CSVs on the web: a primer](http://w3c.github.io/csvw/primer/).

### Developer agreements<a name="agreement"></a>

Developer agreements must be listed in a .csv file named exactly as follows, but with the actual date you created the file instead of YYYYMMDD:

{{< tech-block >}}developer-agreement_YYYYMMDD.csv{{< /tech-block >}}

{{% inset-text %}}
Do not delete or overwrite old or superseded agreements.
{{% /inset-text %}}

#### Column headers:

{{% col-guidance name="developer-agreement" %}}
Create a unique identifier for the agreement. By ‘unique’ this means it should not be used for anything else in your organisation. (You could, for example, use the relevant planning application number appended with a suffix such as ‘-da’.)
{{% /col-guidance %}}

{{% col-guidance name="organisation" %}}
[Find your organisation in this list](https://github.com/communitiesuk/digital-land-data/blob/master/data/organisation.tsv) (in most cases this will be a local planning authority). All text must be in lower case, with no spaces. Norfolk’s local planning authority, for example, would be:

{{< tech-block >}}local-authority:nfk{{< /tech-block >}}
{{% /col-guidance %}}

{{% inset-text %}}
Date fields refer to the recording of the data rather than when agreements come into effect or end – read our data principles on dates for more information.
{{% /inset-text %}}

{{% col-guidance name="entry-date" %}}
Enter the date the agreement was signed and sealed, in the format `yyyy-mm-dd`. For 1 February 2019, for example, you should enter `2019-02-01`
{{% /col-guidance %}}

{{% col-guidance name="start-date" %}}
This will be the same as the entry-date unless the original agreement is superseded by a new version (for example a deed of variation). If so, enter the date on which the new version was agreed, in the same format as the entry-date column.
{{% /col-guidance %}}

{{% col-guidance name="end-date" %}}
Leave this blank if this version of the agreement hasn’t been superseded by a new one. If it has, enter the last day this version was in effect, in the same format as the entry-date column.
{{% /col-guidance %}}

{{% col-guidance name="planning-application" %}}
Enter the unique reference number for the planning application as it appears on the [Planning Portal](https://www.planningportal.co.uk/).
{{% /col-guidance %}}

{{% col-guidance name="document-url" %}}


Enter the web address that links directly to the actual agreement document.
{{% /col-guidance %}}

{{% col-guidance name="developer-agreement-classification" %}}
This is either ‘CIL’ (community investment levy) or ‘S106’ (Section 106). More developer agreement classifications will gradually be added to the developer-agreement-classification.csv file, which MHCLG will maintain for your reference.
{{% /col-guidance %}}

***

### Developer agreement contributions<a name="contribution"></a>

Developer agreement contributions must be listed exactly as follows, but with the actual date you created the file instead of YYYYMMDD:

{{< tech-block >}}developer-agreement-contribution_YYYYMMDD.csv{{< /tech-block >}}

#### Column headers:

{{% col-guidance name="developer-agreement-contribution" %}}
Create a unique identifier for the contribution. If the identifier contains the developer-agreement number it will be easier to quickly identify the contribution as related to the agreement. If the developer-agreement number is ROC100, for example, the developer-contribution could be ROC100-1A.
{{% /col-guidance %}}

{{% col-guidance name="developer-agreement" %}}
Enter the unique identifier you’ve created for the agreement.
{{% /col-guidance %}}

{{% col-guidance name="contribution-purpose" %}}
(Only use this column for Section 106 agreements). Enter the ID for the intended purpose of the developer contribution. This is found in the first column of the developer-contribution-purpose.csv file, which will be held by MHCLG for your reference.
{{% /col-guidance %}}

{{% col-guidance name="amount" %}}
Enter the agreed, secured contribution amount, in pounds and pence but without a currency symbol or commas (for example `100000.00`).
{{% /col-guidance %}}

{{% col-guidance name="units" %}}
If the developer has agreed a non-financial contribution you should quantify that here (eg enter 100 if that many affordable housing units have been promised, 2 for 2 public playgrounds etc).

{{% inset-text %}}
Date fields refer to the recording of the data rather than when agreements come into effect or end – read our data principles on dates for more information.
{{% /inset-text %}}

{{% /col-guidance %}}

{{% col-guidance name="entry-date" %}}
Enter the date the agreement was 'signed and sealed', in the format `yyyy-mm-dd`. For 1 February 2019, for example, you should enter `2019-02-01`.
{{% /col-guidance %}}

{{% col-guidance name="start-date" %}}
This will be the same as the entry-date unless the original agreement is superseded by a new version (for example a deed of variation). If so, enter the date the new version was agreed, in the same format as the entry-date column.
{{% /col-guidance %}}

{{% col-guidance name="end-date" %}}
Leave this blank if this version of the agreement hasn’t been superseded by a new one. If it has, enter the last day this version was in effect, in the same format as the entry-date column.
{{% /col-guidance %}}

***

### Developer agreement transactions<a name="transaction"></a>

Developer agreement transactions must be listed in a .csv file exactly as follows, but with the actual date you created the file instead of YYYYMMDD:

{{< tech-block >}}developer-agreement-transaction_YYYYMMDD.csv{{< /tech-block >}}

#### Column headers:

{{% col-guidance name="developer-agreement-transaction" %}}
Create a unique identifier for the transaction. If the identifier contains the developer-agreement number it will be easier to quickly identify the contribution as related to the agreement. If the developer-agreement number is ROC100, for example, the developer-agreement transaction could be ROC100-TR1.
{{% /col-guidance %}}

{{% col-guidance name="developer-agreement-contribution" %}}
Enter the unique identifier you created for the contribution. 
{{% /col-guidance %}}

{{% col-guidance name="contribution-funding-status" %}}

Enter one of the following to indicate what stage the funding for the contribution is currently in:

* ‘secured’: the trigger clauses associated with the contribution have been met, meaning the developer is now required to pay all or part of the contribution
* ‘received’: the developer has paid the planning authority the money due
* ‘allocated’: the received money has been allocated to a team within the planning authority, who will spend the money
* ‘transferred’: the received money has been transferred to an organisation outside the planning authority (eg Transport for London), who will spend the money
* ‘spent’: the received money has been spent on the agreed contribution purpose (for Section 106) or for Community Infrastructure Levies (CIL) just spent
* ‘returned’: the received money (or a portion of it) has been returned to the developer, for whatever reason

If more than one status applies (eg if some money was spent and some returned), please create a separate row for each status. Fill in each row with all other fields.

{{% /col-guidance %}}

{{% col-guidance name="amount" %}}
Enter the amount of money for each funding status.

Enter the amount as a numeric value eg £10,000 would be entered as `10000.00`

{{% /col-guidance %}}

{{% col-guidance name="units" %}}
If the developer has agreed a non-financial contribution you should quantify how much of that commitment has been met for this transaction (eg enter 50 if 100 affordable housing units were committed and 50 have been delivered).
{{% /col-guidance %}}

{{% inset-text %}}
Date fields refer to the recording of the data rather than when agreements come into effect or end – read our data principles on dates for more information.
{{% /inset-text %}}

{{% col-guidance name="entry-date" %}}
Enter the date the record was created, in the format `yyyy-mm-dd`. For 1 February 2019, for example, you should enter `2019-02-01`.
{{% /col-guidance %}}

{{% col-guidance name="start-date" %}}
Enter the date on which the entry comes into effect, in the same format as the entry-date column.
{{% /col-guidance %}}

{{% col-guidance name="end-date" %}}
Enter the last day the entry is in effect, in the same format as column the entry-date column.
{{% /col-guidance %}}

{{% pagination-component %}}
{{% pagination-prev href="_index.md" text="Publish your developer contributions data" %}}
{{% pagination-next href="update-your-developer-contributions-web-page.md" text="Step 2: Update your developer contributions web page" %}}
{{% /pagination-component %}}