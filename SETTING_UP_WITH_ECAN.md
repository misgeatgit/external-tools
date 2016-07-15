
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
  - (nlp-parse "A sentence here")

 - Connect the visualize and start watching.
 
    
   
