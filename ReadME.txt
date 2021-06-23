Notes when publishing the websites

1. web.config (file): after publishing the site (Web FireAlarm, Web Authentication, Web API) change the "inprocess" to "outofprocess".

2. web.config (file): In these two websites (Web FireAlarm and Web Authentication) paste this 

      <environmentVariables>
        <environmentVariable name="ASPNETCORE_ENVIRONMENT" value="Development" />
      </environmentVariables>
    </aspNetCore>

after </system.webServer> right after "outofprocess">