# GitHub Authentication

1. Go to your GitHub account
2. Go to `Settings`
![Github Settings](./images/github-settings.png)
3. Go to `Developer settings`
![Github Developer Settings](./images/github-developer-settings.png)
4. Go to `OAuth Apps` and click on `New OAuth App`
![Github OAuth Apps](./images/github-developer-settings-auth-app.png)
5. Fill the form fields and click on `Register application`
![Github OAuth App Form](./images/github-developer-settings-auth-app-form.png)
6. Copy the `Client ID` and `Client Secret` and paste in your `application.properties` file
![Github OAuth App Form](./images/github-developer-settings-auth-app-client-and-secrets.png)
```properties
# GitHub OAuth2 configuration
spring.security.oauth2.client.registration.github.client-id=${GITHUB_CLIENT_ID}
spring.security.oauth2.client.registration.github.client-secret=${GITHUB_CLIENT_SECRET}
spring.security.oauth2.client.registration.github.scope=read:user,user:email
``

