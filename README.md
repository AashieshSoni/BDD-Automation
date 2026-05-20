# BDD-Automation
Behavior-Driven Development (BDD) is an Agile software development process that enhances collaboration between technical and business teams by defining system behavior through concrete, 

the below code works for multiple feature files (tags attribute only works when you want to run particular scenario), I tried the below for multiple feature files, it worked:

option 1:
@CucumberOptions(features = {"src\\test\\resources\\cucumberfeaturefolder\\cucumber1.feature",
        "src\\test\\resources\\cucumberfeaturefolder\\cucumber2.feature"},
glue= "StepDef",plugin = { "pretty", "html:target/htmlreports" })


option 2:
 @CucumberOptions(features= "src/main/resources/publish", tags="@Login, @Sendemail",  plugin = { "pretty" },glue= "StepDef" )


option 3:
@CucumberOptions(
        features = {"src/test/resources/features/BeerCans.feature",
                   "src/test/resources/features/multiplication.feature"},
        glue = {"org.example.company.stepfunctions"})
