# Popeye

I had to do a DevOps project, whose goal was to make saved e-line votes.

Five components make up the application:

 * Poll, a Flask Python web application that collects votes and pushes them to a Redis queue.
 * A Redis queue, which holds the votes sent by the Poll application, waiting for them to be consumed by thethe worker.
 * The worker, a Java application that consumes the votes in the Redis queue and stores them in a PostgreSQL database.a PostgreSQL database.
 * A PostgreSQL database, which stores (persistently) the votes stored by the Worker.
 * Result, a Node.js web application that retrieves the votes from the database and displays the result.
