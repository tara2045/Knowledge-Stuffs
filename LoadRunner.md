# Knowledge-Stuffs

Go to Remote Desktop Connection in Windows:
fmdperf115win
account UserId: sa617032
password: Winter17

To open scripts: go to load Generator
To see the test scenario: go to controller




## Basically used for performance test and stress test. 

## Performance test: will be done by giving load(tps) of certain amount and performance of the application will be tested.

## Stress test: will be done by giving load(tps) small at the beginning and then gradually increasing the load and testing the max load handling capacity of the application. 

### TEst details:
Scenario(actual Test with TPS and duration settings):
Y:\Performance\Raptor\rHistory\SCENARIO\2018\Scenario\Scenario_Snaptor_rHistory

Script (you make script changes, example host, template, symbols etc):
Y:\Performance\Raptor\rHistory\SCRIPTS\2018\PerfTest_rHistory_Test_ACTIVMigration

We are making following changes:
We can create two Scripts:
Script 1: host is QA (ACTIV)
1.  Change host in Check_Login() function

Script 2: Host is Dev(MDDS)
1. Modify test to run in dev (mdds)


For report, you need to collect:
Response time summary (table)
Response time chart
Hits per second chart

### Result from Load testing report demo meeting with team:
		-should perform testing keeping only mdds and deploy in dev and run load test.
		- again comment other parts and keep only activ part and deploy in dev and run load test.
		-should do both testing in the dev server only.
		-also compare the total throughput (bytes) which is the size of response and also check the response of both. Both should be same . and also check laod testing
		
### ENABLE OTHER TEMPLATES and SHARE loads between templates:
1. Go to Run-Time Settings
2. Insert actions>> means templates haru add garne(template enable vayeko dekhincha)
3. templates ma click garera ani DELETE garepachi temparality disable huncha template..
4. 100% load lai sharing garne kati wota template ma test garne ho teti wota ma percentage wise badne.. EG: If i have enabled for 4 templates then, we can keep 10,35,35,20 and we can do that by clicking properties.
5. templates sample change garna mann lagyo vane GetTxn vanne line ma gayera change garne.. For eg: GetTxn("{DOMAIN_RR_CLEAR}","/service/historical/chart/lite/json?productid=wealth........


