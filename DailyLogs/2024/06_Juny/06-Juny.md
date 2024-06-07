# Abans de començar
Short term TODOs:
- Reemborsament dels viatges:
	- [ ] NEMO meeting.
Mid term TODOs:
- blenderNC: col·laborar per treure una versió que funcioni amb Blende vº>=4 
Long term TODOs:
- Mixed Precision

# Objectius d'avui

- [ ] Come up with something for the visit at AWI:
	- [x] Check FESOM data.
	      Used Patrick scripts to create a Fesom mesh.
	- [ ] Make an introduction presentation.
	      
	  Nikolay shared my survey to 7 people (8 counting him). Got answers from half of the participants. For now we have that 2/4 never used it and 2/4 consider themselves beginners. However, they have pretty good level with Python and dealing with geo-spatial data.
- [x] CATS Meeting:
      Mario announced that we are hiring a pretty senior guy that used to work with MultIO. 
      We spent a significant amount of time considering gitlab issue organisation things.
      Gladys mentioned that she and Stella are trying to explain model's run time variability and they believe that it might be related with how intel MPI deals with small messages (EAGER or Rendezvous depending on message size). It seems that they try to use an adaptive mode which end's up messing up things.
      
- [x] Verification Meeting:
      We discussed the results of the verification with Kai, Mario, Xavi, Marta and Maitane. We agreed that even if the verification that Kai is running don't show significant differences, we will try to find this differences on the things that seem to pop up at the analysis: that's global quantities such volume, salinity or heat content.
      One possibility is to directly use the restarts to compute these quantities (these are available at monthly frequency). Another option is to run new simulations trying to output these fields. We will also check that the results in MN5 and Lumi are comparable and will use O025 simulations to do so.  
- [x] AutoRPE:
      Maitane had an experiment that ran from the beginning to the analysis without problem. The next step will be to see if the analysis works.

- [ ] NEMO meeting
	- [ ] Entregar les factures.
- [ ] Revisió del paper de compressió.
- [ ] EERIE deliverable:
	- [x] Fer una primera versió basada en les anotacions de DestinE.
	      Vem acordar que puc utilitzar el mateix que teniem a DestinE, puc fer-ho una mica més llarg que la versió que es va reportar basant-me en la versió interna del deliverable.