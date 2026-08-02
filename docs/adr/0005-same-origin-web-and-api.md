# Serve the web application and API from one public origin

Production deployments expose the web application and backend API through one public HTTPS origin, with the API conventionally mounted below `/api`, while the mobile application calls that same API using its bearer credential. This constrains reverse-proxy deployment but keeps the web session cookie first-party, permits a restrictive `SameSite` policy, simplifies CORS, and avoids dependence on third-party cookie behavior.
