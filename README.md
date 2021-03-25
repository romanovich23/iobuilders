# iobuilders

## Tech + Architecture

The idea of this project is to use robust languages, with the capacity to reuse community libraries and, in addition, to include a larger number of people who control the language in order to facilitate contracting.

In terms of architecture, I would use an event-driven one and divide each application into a microservice structure. In addition, I would use DDD along with hexagonal architecture to guarantee the scalability of the application and ensure the use of best practices for future growth of the project.

### Mobile App

I think the most valid options would be:

- PWA
- Hybrid applications (React Native, Flutter)
- Native applications (Android, iOS)

My recommendation would be to use a hybrid application with the **React native framework**, as it allows us to write a single application valid for android/iOS, reducing development and testing time. In addition, being developed in javascript, it will facilitate the contracting of developers and code can be reused for future web oriented developments.

The other alternative would be with _Flutter_. On the positive side, we would gain in performance, but on the negative side, we would lose contracting options, since there are less developers specialized in the Dart language.

### Backend

As specified above, microservices will be developed to separate the business logic. It is recommended to create an API gateway that centralizes all requests from external applications, the wallet part will be split into one service and the token part into another. This will have to be on a private network so that only the API gateway can access it, thus ensuring that the blockchain part is in a secure area.

For the language, I would use any of the **JVM**, as it is a robust language with a large community behind it. As our intention is to have an event-driven architecture, I would do implementation of a message queue like _RabbitMQ_ or _ActiveMQ_. This will give us eventual consistency, so everything we want to audit will be traced.

Our API gateway must have an authentication system based on **OAuth2/JWT** and also implement HTTPS. The applications could be deployed on any VPS, but I recommend studying **AWS** or **Google cloud** for the centralization of tools and facilities that these companies provide.

## Team

The team will be formed by:

- 1x Product owner
- 1x Blockchain specialist. It would be interesting if you had knowledge in any JVM language.
- 1x DevOps. It would be interesting if you have knowledge in any JVM language and AWS/Google Cloud.
- 1x Backend developer. Strong knowledge of any JVM language.
- 1x Front developer. Strong knowledge with React native.
- 1x FullStack developer. Knowledge with React Native or React and with any JVM language.

## Culture

- Agile methodology
- Diary required at first, then may be optional
- Sprint every two weeks
- Organize meetings to increase confidence in the team
- Share knowledge with the team to grow together
