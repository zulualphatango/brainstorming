# brainstorming  
ideas about future projects  

name: relay information from photo  
tag: quality of life improvement  
description:  
  purpose: memorizing all the available relays is pure waste of time,  
  the shelves (all?) have a list with the symbols, although scanned materials are available  
  it might be a nice quality of life improvement to just make a photo with smartphone and have all  
  relevant info at hand  
    
  subtasks:  
    symbol recognition 95%+ accuracy (60-70 class, easy to get data with smartphone videos)  
    scan descriptions/ relevant infos  
    
  optional subtasks  
    show symbols in a list, commonly searched symbols at top,  
  maybe fast reach part differentiated from the all list  
    processed texts with OCR  
    searchable by names, tags maybe or just plain search function  
usefulness: questionable, only if I specialize for relay networks/ I commonly get the task  
  commonly used? 2/3 (1 yes, 2 so-so, 3 no)  
  saved time: couple of minutes  
###########################################################################################################

name: relay network visualisation  
tag: qualaty of life improvement  
description:  
  purpose: the used relay network is huge, most(?) of the network is using standardized shelves,  
  connections, depencies makes it difficult to grasp that which shelf is connected to what, making  
  finding errors complicated. A simple visualizition, a sort of interactive network map might be useful  
  
  subtasks
    automatize the processing of 200(?) pages of a book  
  input is a photo of the circuit, output is the depencies to other shelves 
    search function for shelves
    gui for results
usefulness: questionable, only if I specialize for relay networks/ I commonly get the task  
  commonly used? 2/3 (1 yes, 2 so-so, 3 no)  
  saved time: couple of minutes  
###########################################################################################################

name: relay cabling check  
tag: work process improvement  
description:  
  purpose: in the back of shelves cables are everywhere,  
  eventhough it's rare they are sometimes connected to wrong relays, is it possible to check if it is?  
  that seems to be a rather complex multi-stage problem (at my level), neat, something interesting  
training data: obtainable with smartphone
  
  subtasks:  
  phase one  
    IOs:  
      Ordered list of numbers in csv  
      (like 18, 26 etc., meaning a cable connects 1 and 8, 2 and 6 input/outputs)  
      photo of cables, check if the cables are connected like the list describes it  
    features:  
      high accuracy 95% paired with low false positive (extra work)  
      and negative (leading to that people search for problem somewhere else),   
      thus unkown result are sent to human operator for classification,  
      supervised classification task with two outputs, IsWrong TRUE/FALSE  
    budget for proof of concept: 6 dollars  
      1.5 dollars for male male cables (40p)  
      1.5 dollars for trial board  
      3 dollars for shipment  
  phase two  
    IOs:  
      each shelf have a picture of the circuits that is in an ideal world updated  
      whenever the circuit changes  
      input is a photo of that picture  
      output ordered list of numbers in csv  
      (like 18, 26 etc., meaning a cable connects 1 and 8, 2 and 6 input/outputs)    
    features  
      high accuracy 95% supervised regression problem(?) further search is required  
  phase three  
    description:  
      in a non-ideal world relays have multiple switches, if one yields problem others are used instead,  
      challenge is that the change isn't always documented thus the task would be a back check,
      are the cables connected in a way that relay circuits are recognizable? 
      it might be easier to make it a one stage supervised classification task, the input is of phase one and two and the
      output is isWrong TRUE/FALSE, further search is required
     
personal notes:
try 60,70,80,90,95 percent accuracies, take in account false positives/negatives
this is a proof of concept only, thus not the photos of real equiqment, but
for phase two a trial pad with male-male cables is used, for phase two maybe replicas of the original photos
      
