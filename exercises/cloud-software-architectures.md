# Exercise 1

The application chosen is [IPManager](https://github.com/harvestcore/tfg), which is the one I developed for my final degree project. Composed of a backend and a frontend it offers a light weight solution to manage provisioning, deployment of services and storage of large-scale machine configurations.

Its architecture pattern is a microservice one, whose services are:
- Frontend. It makes API calls to the backend, process and displays all that information.
- Backend. Provides a REST API and a logic capable of managing the data and operations mentioned above.
- Data access. Allows the backend to access all the data stored in a configured MongoDB server.

All the services mentioned above can work independently, with no need to run all of them in the same machine. So:
- The frontend can be run within a Docker container or installed on-premise and only requires a minimal configuration in order to be able to communicate with the backend.
- The backend provides the REST API, so it gives the flexibility of being capable of work without the frontend. And again, it can be run within a Docker container or installed on-premise.
- As the backend just needs the neccessary info to connect to the MongoDB server it can be wherever you want. It can be located in the cloud or on-premise. There is no "special" setup in this case.

# Exercise 2

In fact, frontend and backend were programmed in different programming languages. For the frontend I used TypeScript (since I used Angular framework). In the case of the backend I used Python.

I could have used another languages, for example Go for the backend, or Java for the frontend (I did actually used Java for a Android App that also makes use of the backend component, [IPMdroid](https://github.com/harvestcore/ipmdroid)).

Related to data storage, the choice was clear. Non-relational databases was a must since the data stored does not have strong relationships, the querys to be made are not that complex and the schema of the data stored is not as strong as in relational databases because in some cases it could happen that not all the fields are stored.