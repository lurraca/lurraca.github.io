---
layout: post
title: React Amsterdam 2017 - Conference Recap
---

Whew. Y'all thought I was gone right? I know what you were thinking, "2.5 years without a post, this guy probably is not longer with us. Or maybe he went crazy and is doing Java now."

Anyway... I am back at it again with another post.

Thanks to [Pivotal](https://pivotal.io) and our professional development policy I attended [React Amsterdam 2017](https://react.amsterdam).

In all honesty, my experience and knowledge of React is very limited. I have been playing with it on side projects that haven't gone very far but I plan to keep working on them. But the framework caught my attention as an alternative to Angular, which is what I have been mostly working with in my day job.

I have to say that I was very impressed with the React community, the conference was full of bright and vibrant people, it reminds me of the Ruby/Rails conferences I attended 4-5 years ago. Attendance was **1000+**.

The conference was very well organized, it was a 2-track conference the main React track and the React Native track. I loved this idea, because with multiple tracks I always get conflicted on which talk to attend and as soon I make decision between *Very cool talk by Very Smart Person #1* and *Very cool talk by Very Smart #2* I start overthinking my decision and not able to fully enjoy the talk that I chose to watch. Since my interest in React Native as the moment is non-existent I chose to attend the main track exclusively.

[The Kromhouthal](https://kromhouthal.com/en) was amazing, a former engine factory turned events venue is probably the most unique of all the building of the conferences that I have attended.

The catering of the event could have been better but I think that for an event of that magnitude it could have been way worse.

I know. I know... you want me to get down to business, right? Cool, Now I will give you a small glimpse of my impression of each talk.

### Max Stoiber (KeystoneJS)
**Styling React/ReactNative Applications** [video](https://www.youtube.com/watch?v=bIK2NwoK9xk)

The talk was mostly about styling React applications using the CSS-in-JS way. Max is the co-author of [Styled Components](https://github.com/styled-components/styled-components), this library allows you to write CSS in the components. It removes the need to use the `className` attribute on your elements since the component will have the styles baked in.

Another key concept that he mentioned was the use of *Containers* and *Components*. Containers as in components that are smart, and Components as in components that just know about how they are styled.

### Jessica Chan (Pinterest)
**How Pinterest Switched Their Template Rendering Engine to React** [video](https://www.youtube.com/watch?v=JyD0AUFHQTQ)

Basically why and how Pinterest switched from Django web server and Jinja/Nunjucks template rendering to Node and React.

The main takeaway for me was how they introduced an interim step, of migrating to Nunjucks on the server(Node) and client and then gradually replace Nunjucks with React.

They improved developer experience since they were no longer dealing with multiple languages, platforms. Also gained 20% in performance in the sections of the site that they already migrated.

### Stefano Masini (Balsamiq)
**A Real-World GraphQL Application in Production** [video](https://www.youtube.com/watch?v=6bRFElKG0a8)

Stefano spoke about using GraphQL which provides a lower network footprint as an alternative to REST.

### Robert Haritonov (Zoover) :zap:
**Advanced SSR Caching with React** [video](https://www.youtube.com/watch?v=m_vUUgI0bo8)

Improving response time with Server Side Rendering and Caching.

### Andrey Okonetchnikov (Feedly) :zap:
**Make Linting Great Again** [video](https://www.youtube.com/watch?v=GLdH9SMG97o)

Linting is a big **issue** in software development :stuck_out_tongue_winking_eye:, stats shows that there are 3 millions commit to 'fix indentation' :). He talked about how to include linting tools on your development flow to free yourself from having to make commits for 'fix indentation' or similar and spend your time working on real problems.

These tools include [husky](https://github.com/typicode/husky) for commit hooks and [lint-staged](https://github.com/okonet/lint-staged) to run linter on staged files.

### Ronald van der Kooy (Evision) :zap:
**Generating Your Client Validation Rules** [video](https://www.youtube.com/watch?v=craV534x6Kw)

Migrating outdated stack to a more modern one. React was chosen for front-end because of the simplicity of the component model, easy learning curve, and performance.

Applications are very configuration heavy and have a lot of validation rules, between the choices they had they opted for generation JS off the backend and serve that as static content so React can access it.

### Feather Knee (Netflix) :zap:
**Building Applications for the Studio in the Cloud at Netflix** [video](https://www.youtube.com/watch?v=Ff5kBpx7pe8)

Feather tell us how her team at Netflix approached building a new tool to 'use data to pick best content' and they made some interesting decisions, like keeping it very simple (no redux), ES6 class syntax, container components, unit tests in Enzyme and Jest snapshots, RxJS extensions and leveraging the React ecosystem for helpful libraries.

### Fun With Fiber Custom Renderers (Formidable)
**Fun With Fiber Custom Renderers** [video](https://www.youtube.com/watch?v=oPofnLZZTwQ)

Ken spoke about writing Custom Renderers with the new React Fiber.

### Alex Castillo (Netflix)
**Pushing Bugs to Prod Responsibly with React and Redux** [video](https://www.youtube.com/watch?v=m_vUUgI0bo8)

Alex spoke about how instrumenting data to Exception Tracking tools (Sentry, Airbrake, Rollbar, etc) can make your life help detect issues before your users do, and also give you hints of areas of your application that might need work.

A key takeaway is using Redux Middleware to send instrumentation data to Exception Tracking tools (Redux Middlewares have many other usages, another one he mentioned was to send data to analytics services using [redux-tap](https://github.com/markdalgleish/redux-tap)). He also talks about a Redux Middleware library to help the instrumentation setup with airbrake called [redux-airbrake](https://github.com/alexcastillo/redux-airbrake) that he authored.

### Michele Bertoli (Facebook)
**Test Like It's 2017** [video](https://www.youtube.com/watch?v=m_vUUgI0bo8&t=32265s)

Michele spoke about the challenges that prevent engineers from writing tests, and keep going into the evolution of testing, there seems to be growing opinion among the React community that *Unit Tests* are not as valuable and therefore we should revisit the traditional testing pyramid.

He introduces [Jest](https://github.com/facebook/jest), which is a complete Javascript testing solution, works with React out of the box. One of the main features is Snapshot Testing, which captures snapshots of React trees to simplify UI testing.

A key takeaway from this talk is that we should spend less time writing tests which it's not the same as having fewer tests, it just means that we should use tools that write them for us.

### Nik Graf (Serverless)
**Introduction to ReactVR** [video](https://www.youtube.com/watch?v=m_vUUgI0bo8)

An introduction on [ReactVR](https://facebook.github.io/react-vr/) which is a framework to build VR apps for the browser using javascript. It follows React components model.

### Michel Weststrate (Mendix)
**Complexity: Divide and Conquer!** [video](https://www.youtube.com/watch?v=3J9EJrvqOiM)

*Divide et Impera*. Following the strategy of great conquerors like Julius Caesar and Napoleon, he states that dividing the concerns is the best way of conquering problems.

Michel talk tries to familiarize the audience with *Reactive Programming*, which is basically 'separate the how- from the when question'.

He introduces [Mobx](https://github.com/mobxjs/mobx) a library of his authoring that does state management as a helper to reduce complexity by separating *state* from *view*.

### Forbes Lindesay (Facebook)
**Flow Typing and React Codebase** [video](https://www.youtube.com/watch?v=lk8o7ym29WM)

[Flow](https://github.com/facebook/flow) is a static type checker for JS. He speaks from the perspective of working on a large codebase using Flow. Describes the advantages of using *static analysis*

Static Typing in languages like Java/C# are not *sound*, meaning they allow for `null` to be passed as arguments to functions and assume inside the function that the values are not `null` and that you can access properties of it which lead to bugs. Flow is focused on [soundness](https://wietse.loves.engineering/flowtype-understanding-optionals-and-null-2fa7b98210ce).

Flow vs Typescript, Typescript is a full compiler and Flow are just annotations that are removed by babel.

He finishes with the setup of Flow on a React project and tips and tricks of making your life easier when working with Flow.