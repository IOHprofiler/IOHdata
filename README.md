# IOHdata

Data sets obtained by benchmarking 11 reference algorithms on all 23 test problems in Pseudo-Boolean Optimization (PBO), which is a specalization / instantiation of __IOHexperimenter__. Those 11 reference algorithms are:

* (1+(λ,λ)) GA 
* (1+1) EA_>0 
* (1+1) fGA 
* (1+10) EA_>0 
* (1+10) EA_logNormal 
* (1+10) EA_normalized 
* (1+10) EA_var_ctrl 
* (1+10) EA_{r/2,2r} 
* (30,30) vGA 
* RLS 
* UMDA 
* gHC

Data sets are stored as `R` objects (`.rds` files), organized in the internal data structure `DataSetList` of __IOHnanalyzer__.  
