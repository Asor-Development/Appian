# Create and Train the AI Skill Model: Document Classification
- train AI Skill model to learn based on documents you provide it
- the model has to go through the documents and learn and train itself
- it is a good idea to do this at the start, so when the time comes to implement it into a process, the document classification is already trained and ready to use
    
1. Create a new AI Skill Object
    - select **Document Classification**
2. Create First Model
    - select Create First Model ---> New Document Type
        - Give the document a name
        - give at least 10 documents, the more the better
        - all document should be a unique PDF file
        - Click Create or 
            - Create and Add Another if you want to add another document type andrepeat these steps to add another document type
        - Save Changes
        - Click **Train Model**
3. When the model has finished training, it should have a 100% accuracy and you can Click Publish and Save Changes
4. Use the Classify Documents smart service in Process Model
    - if you are using a robotic task place it just after the Execute Robotic Task node
    - in the Setup tab select the Document Classification AI Skill you want to use
    - in the Data Tab in the Inputs, click the Documents input and for the value property, click the Edit as Expression button and type `todocument(pv!record.recordField)`
    - in the Data tab, in the Outputs, click on the AboveThreshold output, for Target, click the blue plus to create a new process variable and just click OK
        - Repeat the previous step for the BelowThreshold output variable
    - click ok
5. Add Script task
    - after  Classify Documents smart service


https://academy.appian.com/#/online-course-player/07769a88-b0b5-44ee-a08b-8f2200355f87