We have potentially multiple things going on in on excel file

Andy mentioned that we have pipelines that look like the first couple of columns but then it goes into demographics which potentially is linked via the user id in the excel document

G Row - AtsApplicationflowsteps

```sql
select top 100 * from atsApplications where id = 185153

select top 100 * from [dbo].AtsApplicationflowsteps where id =5362
select top 100 * from AtsApplicationFlows where id = 565

select top 100 * 
from [dbo].[AtsApplicationFlowStepConfigurationStepType6KillerQuestionnaires] 
where AtsApplicationFlowStepID = 5362

select top 100 * from killerquestionnaires where id = 300

select top 100 * from KillerQuestionnaireResponses 
where Id = 162566

select top 100 * 
from [dbo].[KillerQuestionnaireQuestionResponses] 
where KillerQuestionnaireResponseId = 162566

-- where KillerQuestionnaireQuestionID in (1129, 1130, 1131, 1132, 1133, 1134, 1141)

select top 100 *
from KillerQuestionnaireQuestionResponses
```

