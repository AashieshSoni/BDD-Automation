# BDD-Automation
Behavior-Driven Development (BDD) is an Agile software development process that enhances collaboration between technical and business teams by defining system behavior through concrete, 

the below code works for multiple feature files (tags attribute only works when you want to run particular scenario), I tried the below for multiple feature files, it worked:

1. to run TestNG test suite from command line
java -Xmx1024m -cp "*" -Denvironment="AAF_test" org.testng.TestNG "testSuites\FirstSuite.xml" > C:\output.txt

2. to run cucumber feature file from command line 
java -Xmx1024m -cp ".:./Data_Sampler_Cucumber_Test_1_lib/*" cucumber.api.cli.Main --glue com.act.afmc.data_sampler.stepdefs RunJupyterNotebook.feature

3. to run rest assured with TestNG file from command line - rest assured with TestNG file 
java -Xmx1024m -Denv="test" -Dtenant="1000001" -Dcucumber.options=" --tags @ZSightrootloc" -cp '*' org.testng.TestNG -testjar *-tests.jar -xmlpathinjar testSuites/contract-test.xml

4:to run multiple feature files 
@CucumberOptions(features = {"src\\test\\resources\\cucumberfeaturefolder\\cucumber1.feature",
        "src\\test\\resources\\cucumberfeaturefolder\\cucumber2.feature"},
glue= "StepDef",plugin = { "pretty", "html:target/htmlreports" })


5.:
 @CucumberOptions(features= "src/main/resources/publish", tags="@Login, @Sendemail",  plugin = { "pretty" },glue= "StepDef" )


6:
@CucumberOptions(
        features = {"src/test/resources/features/BeerCans.feature",
                   "src/test/resources/features/multiplication.feature"},
        glue = {"org.example.company.stepfunctions"})
