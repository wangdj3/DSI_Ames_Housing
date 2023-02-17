# Project 2: Ames Housing Data and Kaggle Challenge



---
## Problem Statement

asdfasfasdfasdfasf

---
## Data Background

Our study uses data from the Ames, Iowa Assessor’s Office \(via [Kaggle](https://www.kaggle.com/) \) "used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010", which contains housing prices and house/property characteristics.  These characteristics are studied and used to create a model that can be used to predict the prices of other homes in the area.


Reference: [data description & source for below Data Dictionary](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).


---
## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|rtype|object|ACT, SAT, CGR|Record Type: C=County\| D=District\| S=School\| X=State|
|sname|object|ACT, SAT, CGR|School Name\| N/A = County or District Level Record|
|dname|object|ACT, SAT, CGR|District Name\| N/A = County Level Record|
|cname|object|ACT, SAT, CGR|County Name|

#### Originating from the ACT dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|id|int|train.csv, test.csv|identifier used |
|lot_frontage|int|train.csv, test.csv|Linear feet of street connected to property|
|lot_area|int|train.csv, test.csv|Lot size in square feet|
|utilities|int|train.csv, test.csv|(Ordinal): Type of utilities available<br>4	All public Utilities (E,G,W,& S)<br>3	Electricity, Gas, and Water (Septic Tank)<br>2	Electricity and Gas Only<br>1	Electricity only|
|land_slope|int|train.csv, test.csv|(Ordinal): Slope of property|
|overall_qual|int|train.csv, test.csv|(Ordinal): Rates the overall material and finish of the house|
|overall_cond|int|train.csv, test.csv|(Ordinal): Rates the overall condition of the house|
|||||
|year_built|int|train.csv, test.csv|Original construction date|
|year_remod/add|int|train.csv, test.csv|Remodel date (same as construction date if no remodeling or additions)|
|exter_qual|int|train.csv, test.csv|(Ordinal): Evaluates the quality of the material on the exterior|
|exter_cond|int|train.csv, test.csv|(Ordinal): Evaluates the present condition of the material on the exterior|
|bsmt_qual|int|train.csv, test.csv|(Ordinal): Evaluates the height of the basement|
|bsmt_cond|int|train.csv, test.csv|(Ordinal): Evaluates the general condition of the basement|
|bsmt_exposure|int|train.csv, test.csv|(Ordinal): Refers to walkout or garden level walls|
|bsmtfin_type_1|int|train.csv, test.csv|(Ordinal): Rating of basement finished area|
|bsmtfin_sf_1|int|train.csv, test.csv|Type 1 finished square feet|
|bsmtfin_type_2|int|train.csv, test.csv|(Ordinal): Rating of basement finished area (if multiple types)|
|bsmtfin_sf_2|int|train.csv, test.csv|Type 2 finished square feet|
|bsmt_unf_sf|int|train.csv, test.csv|Unfinished square feet of basement area|
|total_bsmt_sf|int|train.csv, test.csv|Total square feet of basement area|
|heating_qc|int|train.csv, test.csv|(Ordinal): Heating quality and condition|
|electrical|int|train.csv, test.csv|(Ordinal): Electrical system|
|1st_flr_sf|int|train.csv, test.csv|First Floor square feet|
|2nd_flr_sf|int|train.csv, test.csv|Second floor square feet|
|low_qual_fin_sf|int|train.csv, test.csv|Low quality finished square feet (all floors)|
|gr_liv_area|int|train.csv, test.csv|Above grade (ground) living area square feet|
|bsmt_full_bath|int|train.csv, test.csv|Basement full bathrooms|
|bsmt_half_bath|int|train.csv, test.csv|Basement half bathrooms|
|full_bath|int|train.csv, test.csv|Full bathrooms above grade|
|half_bath|int|train.csv, test.csv|Half baths above grade|
|bedroom_abvgr|int|train.csv, test.csv|Bedrooms above grade (does NOT include basement bedrooms)|
|kitchen_abvgr|int|train.csv, test.csv|Kitchens above grade|
|kitchen_qual|int|train.csv, test.csv|(Ordinal): Kitchen quality|
|totrms_abvgrd|int|train.csv, test.csv|Total rooms above grade (does not include bathrooms)|
|functional|int|train.csv, test.csv|(Ordinal): Home functionality (Assume typical unless deductions are warranted)|
|fireplaces|int|train.csv, test.csv|Number of fireplaces|
|fireplace_qu|int|train.csv, test.csv|(Ordinal): Fireplace quality|
|garage_yr_blt|float|train.csv, test.csv|Year garage was built|
|garage_cars|int|train.csv, test.csv|Size of garage in car capacity|
|garage_area|int|train.csv, test.csv|Size of garage in square feet|
|garage_qual|int|train.csv, test.csv|(Ordinal): Garage quality|
|garage_cond|int|train.csv, test.csv|(Ordinal): Garage condition|
|paved_drive|int|train.csv, test.csv|(Ordinal): Paved driveway|
|wood_deck_sf|int|train.csv, test.csv|Wood deck area in square feet|
|open_porch_sf|int|train.csv, test.csv|Open porch area in square feet|
|enclosed_porch|int|train.csv, test.csv|Enclosed porch area in square feet|
|3ssn_porch|int|train.csv, test.csv|Three season porch area in square feet|
|screen_porch|int|train.csv, test.csv|Screen porch area in square feet|
|pool_area|int|train.csv, test.csv|Pool area in square feet|
|pool_qc|int|train.csv, test.csv|(Ordinal): Pool quality|
|fence|int|train.csv, test.csv|(Ordinal): Fence quality|
|misc_val|int|train.csv, test.csv|$Value of miscellaneous feature|
|saleprice|int|train.csv|Sale price $$|

#### One-Hot-Encoded Variables (prefix-)
|Feature|Type|Dataset|Description|
|---|---|---|---|
|ms_subclass|int|train.csv, test.csv|Identifies the type of dwelling involved in the sale.<br><br>020	1-STORY 1946 & NEWER ALL STYLES<br>030	1-STORY 1945 & OLDER<br>040	1-STORY W/FINISHED ATTIC ALL AGES<br>045	1-1/2 STORY - UNFINISHED ALL AGES<br>050	1-1/2 STORY FINISHED ALL AGES<br>060	2-STORY 1946 & NEWER<br>070	2-STORY 1945 & OLDER<br>075	2-1/2 STORY ALL AGES<br>080	SPLIT OR MULTI-LEVEL<br>085	SPLIT FOYER<br>090	DUPLEX - ALL STYLES AND AGES<br>120	1-STORY PUD (Planned Unit Development) - 1946 & NEWER<br>150	1-1/2 STORY PUD - ALL AGES<br>160	2-STORY PUD - 1946 & NEWER<br>180	PUD - MULTILEVEL - INCL SPLIT LEV/FOYER<br>190	2 FAMILY CONVERSION - ALL STYLES AND AGES|
|ms_zoning|int|train.csv, test.csv|Identifies the general zoning classification of the sale.<br><br>A	Agriculture<br>C	Commercial<br>FV	Floating Village Residential<br>I	Industrial<br>RH	Residential High Density<br>RL	Residential Low Density<br>RP	Residential Low Density Park<br>RM	Residential Medium Density|
|street|int|train.csv, test.csv|Type of road access to property<br><br>Grvl	Gravel<br>Pave	Paved|
|lot_shape|int|train.csv, test.csv|(Ordinal): General shape of property<br><br>3	Regular<br>2	Slightly irregular<br>1	Moderately Irregular<br>0	Irregular|
|land_contour|int|train.csv, test.csv|Flatness of the property<br><br>Lvl	Near Flat/Level<br>Bnk	Banked - Quick and significant rise from street grade to building<br>HLS	Hillside - Significant slope from side to side<br>Low	Depression|
|neighborhood|int|train.csv, test.csv|Physical locations within Ames city limits|
|bldg_type|int|train.csv, test.csv|Type of dwelling<br><br>1Fam	Single-family Detached<br>2FmCon	Two-family Conversion; originally built as one-family dwelling<br>Duplx	Duplex<br>TwnhsE	Townhouse End Unit<br>TwnhsI	Townhouse Inside Unit|
|house_style|int|train.csv, test.csv|Style of dwelling<br><br>1Story	One story<br>5Fin	One and one-half story: 2nd level finished<br>5Unf	One and one-half story: 2nd level unfinished<br>2Story	Two story<br>2.5Fin	Two and one-half story: 2nd level finished<br>2.5Unf	Two and one-half story: 2nd level unfinished<br>SFoyer	Split Foyer<br>SLvl	Split Level|
|roof_style|int|train.csv, test.csv|Type of roof<br><br>Flat	Flat<br>Gable	Gable<br>Gambrel	Gabrel (Barn)<br>Hip	Hip<br>Mansard	Mansard<br>Shed	Shed|
|central_air|int|train.csv, test.csv|Central air conditioning|
|garage_finish|int|train.csv, test.csv|Interior finish of the garage|
|mo_sold|int|train.csv, test.csv|Month Sold (MM)|
|yr_sold|int|train.csv, test.csv|Year Sold (YYYY)|


---
## Primary Findings

- Top (individual) factors correlated with saleprice appear to be: overall_qual, exter_qual, gr_liv_area, kitchen_qual, garage_area.<br><br>
It stands to reason that for a person hoping to increase their home sale value, these would be the areas of focus.

- Top higher-order (3rd degree polynomial) factors correlated with saleprice are listed in the table below




### Most Influential features in higher order (3rd degree polynomial) model:

#### Top most POSITIVELY influential features in final model
||Feature Description|scaling power (non-dimensional)|
|---|---|---|
|1|(overall_qual exter) * (qual bsmt_qual)|5786.106282|
|2|(overall_qual) * (full_bath kitchen_qual)|5328.531647|
|3|(overall_qual)^2 * (garage_cars)|5243.503826|
|4|(overall_qual)^2 * (garage_cars)|5243.503826|
|5|(heating_qc) * (gr_liv_area functional)|3898.87032|
|6|(overall_qual) * (garage_cars) * (garage_area)|3275.160347|
|7|(overall_cond) * (gr_liv_area functional)|3265.027374|
||||

#### Top most NEGATIVELY influential features in final model
||Feature Description|scaling power (non-dimensional)|
|---|---|---|
|-1|(mas_vnr_area) * (total_bsmt_sf) * (neighborhood_Edwards)|-5858.773851|
|-2|(total_bsmt_sf) * (garage_area) * (neighborhood_Edwards)|-4979.10532|
|-3|(mas_vnr_area) * (bsmtfin_sf_1) * (neighborhood_Edwards)|-3049.396129|
|-4|(bsmtfin_sf_1) * (mo_sold_1) * (yr_sold_2009)|-1170.813491|
|-5|(fireplaces) * (open_porch_sf) * (neighborhood_Edwards)|-899.948678|
|-6|(lot_area) * (foundation_BrkTil) * (mo_sold_8)|-716.521048|
|-7|(screen_porch) * (yr_sold_2010) * (garage_type_Detchd)|-709.927402|
||||

---
## Comments/Instructions for Graders

- All data processing, EDA, and modeling are contained in the same notebook: 'dw-final.ipynb'.  The input and contest files are processed differently by the code depending on whether the run_type variable at the top is set to a 1 or non-1 value.

- Cleaned datasets as well as the original source data files utilized can be found in the './datasets' directory 

- Model-generated output filescan be found in the './output' directory 


---
## Sources & References

1.[Kaggle](https://www.kaggle.com/)
2.[data description & source for below Data Documentation](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).

