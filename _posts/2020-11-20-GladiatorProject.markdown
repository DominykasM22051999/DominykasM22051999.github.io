---
layout: post
title:  "Gladiator Game Project"
date:   2020-11-20 19:48:32 +0000
---
### <u>Overview</u>
This project is a browser gladiator game the expected release of the MVP is early 2021. The team consists of four people
with varied experience.

**Workflows used**: Git and Agile. **Technologies used**: JavaScript, Node.js, MongoDB, Discord.js.

**Note**: Due to the project being in a private repository I am not able to share any code within the project.

### <u>Contributions</u>

#### <u>Opponent List and Opponent Preview</u>
Developed the OpponentList screen which displays the logged in user, retrieved users, and bots from the database to the user who they can
then choose to fight. The refresh button communicates with the database to retrieve a mixture of bots and other players.
From the list the user can then select an opponent they would like to fight by clicking the red sword. The user is then
displayed with the preview of the opponent with their stats. If the fight button is clicked the user is taken to the
arena with the gladiator.
<figure>
    <IMG SRC="{{ site.baseurl }}/assets/OpponentList.gif">
</figure>
<div align="center">(Reference: 24/11/2020)</div>

#### <u>Attribute Allocation System</u>
Once a user levels up we want the user's gladiator to get stronger, so the user can choose between four stats that
they can allocate the attribute point towards. If the user decides to retrieve that point and use it for another skill
they are free to do so. Once the user clicks confirm the new stats and attribute points are updated in the database.
<figure>
    <IMG SRC="{{ site.baseurl }}/assets/AttributePoints.gif">
</figure>
<div align="center">(Reference: 24/11/2020)</div>

#### <u>Generated 10,000 bots to the database</u>
Generated 10,000 records of bots to the database. These bots have attribute points randomly assigned to them in a
decimal format so when the user levels up the bots also get stronger. This is evident in the opponent list screen
that I have made as the user is always matched with some players and bots of his gladiators' strength.
<figure>
    <IMG SRC="{{ site.baseurl }}/assets/bots.png">
</figure>
<div align="center">(Reference: 24/11/2020)</div>

#### <u>Swagger documentation for every Swagger endpoint (WIP)</u>
I am currently working on documenting every endpoint of the server using Swagger OpenAPI 3.0 for the game server. 
This will prepare me for a possible future side project of the game and by knowing all the server endpoints it will 
prepare me for it. The side project mentioned is not yet decided but in the stage of discussion. Utilising Spotlight
Studio in this task to assist with creating every path, and model.
{% highlight ruby %}
openapi: 3.0.1
info:
  title: GLAD Server
  description: HelloWorld
  contact:
    name: Noob Squad
  license:
    name: Apache 2.0
    url: 'http://www.apache.org/licenses/LICENSE-2.0.html'
  version: 1.0.0
servers:
  - url: 'http://localhost:8080/v1'
paths:
  /gladiators:
    get:
      summary: Get Gladiators
      tags:
        - gladiators
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema:
                type: object
                properties:
                  status:
                    type: string
                  data:
                    type: array
                    items:
                      $ref: '#/components/schemas/Gladiator'
      operationId: get-gladiators
      parameters: []
      description: Returns list of gladiators
{% endhighlight %}
<div align="center">(Example of one path: /gladiators - Reference: 24/11/2020)</div>

#### <u>Bug fixing</u>
Actively participating in testing and reviewing not only my code but also the rest of the team. Some examples of bugs
that I have fixed are when the user spams the refresh button (as seen above in opponent list) the FPS will drop, user
health was not reset after battle correctly, resetting frame on level up animation if a user leveled up more than once.

#### <u>Creation of gladbot</u>
Created a Discord bot in the Discord server of the team to display each member's  ID, username, tag, and created_at
time.