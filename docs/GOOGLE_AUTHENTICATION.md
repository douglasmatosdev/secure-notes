# Google Authentication
1. Search for Google Cloud Console
![Search google cloud console](./images/google-cloud-console-search.png)
2. In the Google Cloud Console, click create project
![Create Project](./images/google-cloud-console-create-project.png)
3. Go to `APIs & Services`
![APIs & Services](./images/google-cloud-console-api.png)
4. Go to `credentials` and select OAuth client ID
![Credentials](./images/google-cloud-console-api-client-id.png)
5. Go to `OAuth consent screen`
![OAuth consent screen](./images/google-cloud-console-api-configure.png)
6. Select `External` and click create
![Credentials](./images/google-cloud-console-api-configure-external.png)
7. Fill in the necessary details and click save
![OAuth consent screen](./images/google-cloud-console-api-configure-screen-oauth.png)
8. Go to `OAuth consent screen` and click on `Add Scopes`
![OAuth consent screen](./images/google-cloud-console-api-configure-screen-oauth-scopes.png)
9. Create user tests
![OAuth consent screen](./images/google-cloud-console-api-configure-screen-oauth-user-tests.png)
10. Configure OAuth App
![OAuth consent screen](./images/google-cloud-console-api-configure-oauth-app.png)
11. Fill in the necessary details and click save
![OAuth consent screen](./images/google-cloud-console-api-configure-oauth-app-form.png)
12. Save the client ID and client secret
![OAuth consent screen](./images/google-cloud-console-api-configure-oauth-app-id-secret-key.png)
13. Put the client ID and client secret in the `application.properties` file
```properties
# Google OAuth2 configuration
spring.security.oauth2.client.registration.google.client-id=${GOOGLE_CLIENT_ID}
spring.security.oauth2.client.registration.google.client-secret=${GOOGLE_CLIENT_SECRET}
```