## Technical Challenge

> ### In order for us to evaluate your technical performance, develop the test described in this document from best possible way, applying Object Orientation, Clean Code, SOLID, Design Patterns, Mult-layered and Multi-Tiered techniques and making the most of your potential.

- 1. [Create database with below file structure (preferably in PostgreSQL).](./script.md)
- 2. Define three-tier system architecture.
  - Rest communication with JSON between Client/Server application
  - Apply Clean Code
  - Object orientation
  - Design Standards
  - Ensuring integrity between records (no person without an address)
  - Persistence layer, use Firedac
- 3. Develop a registry of people
  - The objective is to make a simplified registration with the person's data and the zip code (in item 4 to
address_integration table will be updated based on the entered zip code).
  - Tables
    - Person and Address
  - Methods
    - Insert.
    - Update.
    - Delete.
    - Insert in batch (new method): receives a list of people (assuming that
      this list can have 50,000 records. Adopt a strategy for the
      insertion of these records is performative).
- 4. Develop new routine using Threads.
    - Objective is to update the addresses of people registered in item 3.
    - For each record in the address table, read the CEP field and integrate with the “API
      via cep” through the URL viacep.com.br/ws/_numero_CEP/json/.
      - Use zip code field from address table.
    - Update the fields of the integration_address table with the return JSON data.

> ### Rating criteria
1. Use PostgreSQL as a database.
2. Use FireDAC to connect to the database.
3. Use transaction and exception handling concepts when writing data.
4. Make sure you write your code, because the formatting is being evaluated.
5. Use object-oriented concepts, creating classes for example.
6. Do not use 3rd party components, always use what is native to the IDE.

