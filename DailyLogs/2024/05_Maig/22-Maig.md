# Abans de començar
# Abans de començar
# Abans de començar
Short term TODOs:
- 
- Reemborsament dels viatges:
	- [ ] W2W **URGENT**
Mid term TODOs:
- blenderNC: col·laborar per treure una versió que funcioni amb Blende vº>=4 
Long term TODOs:
- Mixed Precision

# Objectius d'avui

- [ ] Reemborsament dels viatges:
	- [ ] W2W **URGENT** mirar quin document he d'omplir i omplir-lo.
	      Ja tinc la factura de lufthansa. Omplir document i enviar-lo a la Barbara.
- [ ] Come up with something for the visit at AWI:
- [ ] AutoRPE:
	- [ ] Make AutoRPE work with:
		- [ ] NEMO 5.0:
			- [x] Fix problems with variable case sensitivity.
			- [x] Fix problem with subroutines that don't have the name at the "end subroutine"
			- [x] Fix edge case for get_dimension_of_contents with a keyword argument with a logical comparison: 'ldfin=(jk == jpkm1)
			- [x] Fix problem with variables wrongly identified as functions.
			      Fix in CallManager.py
			- [x] Fix for: No matching routine found for interface : mpp_min
			      This arises from a problem interpreting properly the dimension of an array: 'REAL(sp), DIMENSION(SIZE(ptab,3)) ' is interpreted as dimension 2 instead of dimension 1.
		     - [x] Fix problem with dimensions: 'REAL(sp), DIMENSION(SIZE(ptab,3)) '
		     - [x] No matching routine found for interface : lbc_lnk
		           Looks like the interface does not have procedures for 0d and 1d variables. Probably I broke something with the previous fix because the arguments shouldn't have dim=0 but dim=2. 
		           In fact that was the case, the function didn't handle properly a space between dimension and the parentheses. Now it was fixed.
			- [x] Got the error message: Please add the type specification for this intrinsic: IOR.
			- [x] Fix: Something went wrong finding the dimension of AIMAG(todelay(ji)%ydpbuffout).
			       messed up adding the type  of AIMAG
			- [ ] Problems finding the type of: 'frcv(jpr_taum)%z3(Nis0-(0):Nie0+(0),Njs0-(0):Nje0+(0),1)'
		           Happens at the Fixing modules stage.
			      
		- [ ] NEMO 4.2.2
