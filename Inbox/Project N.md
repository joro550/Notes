Job by job extract that have different steps 
each job has different amount of steps

things that might look similar are not similar

Each step of the role
- status
- score
- result

Try not to mimic the excel document

Progress table - status at that point in time 

Demographics against member (back in the day)
maybe against application questionnaires (this is a guess)

What do they want exactly? 

The results could have a 'key' to tell you what sort of question it might be i.e. might be asking for gender in 100 different ways but the key helps you 'fan it in' to one question

stream lit - some sort of library 

What do we do to generate this data?
How do we solve each of the issues


-----

for each steps would we want to pivot? 
- for each step pass/fail


----

3 years of data

---

- [x] Names
- [ ] Responses to a questionnaire
	- [ ] Contact details (application form)
	- [ ] Right to work (application form)
- [ ] Responses to particular questionnaire 
	- [ ] Education (application form)
- [ ] STG_APPLICATION_OFFERS
	- [ ] Offers /offer status
- [ ] Flagged status (per role and per stage – Capp/Onestop, Simulate, AC and offer)
- [ ] Flagged status (per demographic – gender, ethnicity, disability per stage)
- [x] Gender
- [x] Ethnicity
- [x] Disability
- [ ] Volumes per role per stage – we’ll have volumes but we’ll need to know the role someone has applied to from the ATS.

---

for the ats that'd either refer to a step - see STG_APPLICATION_FLOW_STEPS

steps can be grouped together in the ats and this, for nestle, this might be what they mean - see STG_APPLICATION_FLOW_STEP_GROUPS

I guess the data could be diced by either tbh...if the group name is included could aggregate on it etc

anything that states application form would probably come from the STG_APPLICATION_QUESTIONNAIRE_* tables

a lot of the application form bits listed would be a question - not sure how identifiable they are i.e. how to know that some states they are male/female unless they use the lookups feature

education would probably come from STG_APPLICATION_QUESTIONNAIRE_QUALIFICATIONS although the feature is flexible and some people might configure it without that feature

flagged = STG_APPLICATIONS.IS_FLAGGED

offer status partly from STG_APPLICATIONS.IS_JOB_IN_OFFER but probably STG_APPLICATION_OFFERS using the application id and then there's a STATUS/STATUS_DESC column

demographics I'm pretty sure would come from an application form but they could choose to capture that outside of the ats i.e. in a captivate...depends on the client

signing off in a second, give me a shout tomorrow if you need


---

when do we write an offer status into the ats 
what makes a questionnaire an application form is it literally just a group name or can we make other assumptions about the group name

- candidate 
	- status 
	- scores <-
	- right to work <-
	- education <-
- job offer status
	- demographics
		- sexual orientation
		- ethnicity

offer status for each record not a thing
