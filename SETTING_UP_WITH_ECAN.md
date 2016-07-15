
###Visualizing the attentional focus with ECAN###

*Steps*

- start cogserver
- Start the REST server according to the steps stated [here](http://wiki.opencog.org/w/REST_API)
- Start the ECAN system in the opencog shell (i.e telnet localhost 17001) 
  - loadmodule $OPENCOG_BASE_DIR/opencog/build/opencog/attention/libattention.so
  - agents-start opencog::SimpleImportanceDiffusionAgent
  - agents-start opencog::ImportanceUpdatingAgent
- Parse a sentence
  - (use-modules (opencog) (opencog atom-types) (opencog persist-pgsql) (opencog openpsi)(opencog nlp relex2logic)(opencog rule-engine) (opencog query) (opencog nlp chatbot))
  - (nlp-start-stimulation [some amount])  lets use 60 for some amount
  - (nlp-parse "A sentence here")

 - Connect the visualize and start watching.
 
 *Note* - This visualizer is kind of a hack. All it does is refresh every 5sec and display fixed size random atoms from the AF. The reason we wanted fixed set of rando atoms is that to solve the cluttered display problem.
 
    
   
