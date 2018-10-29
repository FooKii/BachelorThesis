Under this Git are my python scripts for the simulation of different collision-resolving algorithms

[26.07.18] Coding the initalisation of n random IDs in binary. To test if IDs are unique to each other, i initialised with 8 IDs in length of 3 bits(upper limit), it returns 8 
           unique Ids from 0 to 7. Then i tested with 9 IDs in length of 3(over limit), the programm ran into a deadloop, which means the function can ensure the uniqueness of IDs.

[29.07.18] Coded the queryTree using given Algorithm from Paper 6. Works good and easy.

[30.07.18] Coded the SICTA simulation, create and conceive the algotirhm on the gateway side! very hard and debugged for 8 hours. Now its working good and for active user under 1000, the calculation will be done under 5 secs. for active users over 10000, takes way too long

[01.08.18] Combined the SICTA and QT together, and fixed some bugs on SICTA(k calculation). all 3 algorithms works fine individually, but seems that SICTA and SICQA has some variable crush, so they cant run together. This need to be fixed tomorrow.

[03.08.18] fixed the crush of running all 3 algorithms at the same time under one ID_list. The reason is that list.append in python refers to a mutable variable. That's to say: After received.append(ID_list), if some changes occurs to 'received', the ID_list will be changed as well.
Added matplot to visualise the results, the SICQTA show better stability(low max T) and by large amount of active IDs, it shows even better average and min T. For each test group, the results are all listed in the .txt file.

[05.08.18] added comments 

[08.08.18] improved SICTA by deleting sicta_id after the element is decoded