# census_data_extraction

##### do the preliminary work

* Open Excel file GIS_Census.xlsx  
<br>
* You are expected to change the data input. However, do not change column names and the order by which the parameters are displayed. Furthermore, do not write anything on the areas highlighted in gray.  
<br>
* In the "parameters tab", fill parameters according to your needs.  Nontheless, you must remember the following:  
    
1. *If you are using "acs1" the summary level CANNOT be 140. "acs1" type is less granular, so 050 and 040 are the only levels available.*  
    <br>
2. *You CANNOT mix certain table types, so you should download every type separately. For example, your "logic tab" CANNOT have at the same time the following attributes B25002_001E (a detail attribute from a detail table) and DP03_0001E (a detail attribute from a profile table) because the script will fail.*  
    <br>
3. *Adjust parameter table according to the data type you are using. Options are ‘detail’ (detail tables), ‘subject’ (subject tables), ‘profile’ (data profile tables), ‘cprofile’ (comparison profile tables).*  
    <br>
4. *Adjust your the "Naming Friendliness" parameter by using the most appropiate logic column name for your work.  For instance, a GIS analyst would be more interested in pulling data with "GIS Name" column names.  Options are ‘Schema Name’ (the census coded names), ‘Human Friendly Name’ (the human names assigned by the census bureau), ‘Mgr_Name’ (names assigned by the team of researchers), and ‘GIS_Name’ (names created by the GIS analyst to create a visualizations).*  
    <br>
<br>    
* In the "logic tab", fill parameters according to your needs.  Nontheless, you must remember the following:  

    1. *The "logic tab" MUST have NO data gaps.  This means that each schema name MUST have a human friendly name, mgr_name, a GIS_name and a description.  If you have no definition at hand, you should type down "No Definition".  This script uses this information not only to pull the data from the census bureau, but also to document the data search.  This script will delete ALL lines that are NOT complete.*
<br>
<br>
* You can pull data until 2011. However, you should be aware that the census bureau work is dynamic, which means that attributes that are tracked in 2019 are NOT necessarily available in previous year.  The script will throw an error message when the attribute does NOT exist.  
<br>
<br>


##### if  you are NOT sure about the table type you are dealing with    
    
The American Community Survey (ACS) provides four different sets of data tables:

* **Detailed tables**. These provide the most detailed set of variables. Table names begin with B followed by a numeric code.  

* **Data profile tables**. These tables are designed to provide information on a broad array of characteristics for a given geography. There are data profile tables on:  

    1. Social Characteristics (DP02),
    1. Economic Characteristics (DP03),
    1. Housing Characteristics (DP04), and
    1. Demographic Characteristics (DP05).  
    
  Table names (beginning in DP) are shown in parentheses above.  
  
 <br>

* **Subject tables**. These tables are designed to provide information on narrower topics for a broader range of geographies. Table names begin with S.

* **Comparison profile tables**. These tables provide information on changes in characteristics in particular geographies over time, including statistical significance testing. Table names begin with CP.
<br>
<br>


##### if  you are NOT sure about the summary level you are looking for 

This file only provides data for State, State-County and State-County-Census Tract.  To learn more bout the cartographic boundary file summary level, go visit:  
<br>
https://www.census.gov/programs-surveys/geography/technical-documentation/naming-convention/cartographic-boundary-file/carto-boundary-summary-level.html
