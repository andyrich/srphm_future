Model files provided by usgs/alzriaee. 
Updated by A. Rich, 1/26/2019.

Converting to GSFLOW5 in order to use dynamic parameters

need to add:
tmax_allrain_offset

Summary:
Ag package added to model.
Dynamic parameters added.

Well file removed because of files size for now.

Switched from GSFLOW 4 to GSFLOW 5
increased soil_moist_max by 2x (for active crop HRU's)
increased sat_threshold by 2x (for active crop HRU's)
However, because dynamic parameter capability in GSFLOW currently has bug, soil_moist_max is set to 2x for entire simulation if there is EVER a vineyard in that location. All other locations remain default value.
Added dynamic parameter for imperviousness. Data from NLCD. Dates of change are 2001, 2005, 2011, 2016. Earlier dates (1974, 1986) currently being processed by SCWA. SRPHM 1.0 used a constant 2008 dataset.
Used crop coefficients for each crop to create dynamic parameter input for all crops for all stress periods.
Changed ‘srain_intcp’ to zero for vineyards. Srain_intcp controls amount of intercepted precipitation [irrigation] to account for drip irrigation.
Changed covden to a constant 0.2. covden represents the % of HRU covered by vegetation.
Changed soil_rechr_max_frac to 0.4. Value represents the fraction of the capillary zone available to evaporation and transpiration. Remaining portion of soil zone only allows transpiration.
Set initial values for soil moisture.


