SLN Files (using Visual Studio) are the files where you can access the other files (repositories) such as..
- Identity Server Ibiz (Website Authentication)
- FireAlarmResponse (Mobile Application)
- ArduinoAPISample (Web API gateway between the websites, Arduino boards, and the mobile application)
- WebFireAlarmArduino (Website Activities/Context/Contents)

Notes when publishing the websites

1. after publishing a project, locate that specific folder (Web Activities, Web Authentication, annd Web API) and change the "inprocess" to "outofprocess" and remove the "/".
2. find web.config file and open it in Visual Studio and replace the "inprocess" to "outofprocess".
3. then in these two websites (Web activities and Web Authentication) before </system.webServer> right after ..."outofprocess"/>

paste the following
 
      <environmentVariables>
        <environmentVariable name="ASPNETCORE_ENVIRONMENT" value="Development" />
      </environmentVariables>
    </aspNetCore>

