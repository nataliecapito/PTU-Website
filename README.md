# Real project found here: https://github.com/d13kotson/PTU-Website

#
#
#

# General
- Pokemon DnD digital spreadsheet! Let's GO!

# Init. Build and Run
- Add the secret key to: `tabletop/settings.py`
- Install python dependencies: `pip3 install -r requirements.txt`
- Install npm dependencies: `npm install`
- Build the react project: `npm run build:dev`
- Add these: `python3 manage.py collectstatic`, `python3 manage.py makemigrations ptu maps chat`, `python3 manage.py migrate`, `python3 manage.py loaddata db.json`
- Create a user: `python3 manage.py createsuperuser`
- Run the Django server: `npm run start`
- Available at your: http://localhost:8000/

# Compiling
- `npm run start` -> Runs the Django server.
- `npm run build:prod` -> Bundles the app into static files for production.
- `npm run build:dev` -> Bundles the app into static files for development.

# Importing data
- This project includes a db.json file. This contains example data for the Pokemon Tabletop United system. It can be imported with `manage.py loaddata db.json`.

- You will need to migrate before you can load the data. `manage.py makemigrations chat maps ptu` will create all necessary migrations and `manage.py migrage` will apply them.

# High level project layout
## accounts
- The Django app for creating user accounts and logging in.

## chat
- The Django app for the chat service.

## frontend
- The React app for the entire UI of the web app and the Django app that serves it.

## maps
- The Django app for the map service.

## ptu
- The Django app for the rest API used to deal with character and Pokemon data.

## tabletop
- The Django project level settings.

# Frontend
- The frontend of the app is a little all over the place. It is served by Django, so the the React code itself is in frontend/src.

- The React components are grouped roughly according to how they are nested.

# API Endpoints
* /trainers/ - Returns a list of all trainers associated with the logged in user.
* /trainers/\<int:game> - Returns a list of all trainers associated with provided game id.
* /wildpokemon/\<int:game> - Returns a list of all Pokemon associated with the provided game id witout trainers.
* /games/ - Returns a list of all games with the logged in user as the GM.
* /edges/ - Returns a list of all Edges in the DB.
* /features/ - Returns a list of all Features in the DB.
* /attacks/ - Returns a list of all Attacks in the DB.
* /species/ - Returns a list of all Pokemon Species in the DB.
* /attack/\<int:pk> - Returns all information for the provided Attack.
* /edge/\<int:pk> - Returns all information for the provided Edge.
* /evolution/\<int:pk> - Returns all information for the provided Evolution.
* /feature/\<int:pk> - Returns all information for the provided Feature.
* /game/\<int:pk> - Returns all information for the provided Game.
* /item/\<int:pk> - Returns all information for the provided Item.
* /pokemon/\<int:pk> - Returns all information for the provided Pokemon.
* /pokemonAttack/\<int:pk> - Returns all information for the provided Pokemon Attack.
* /species/\<int:pk> - Returns all information for the provided Species.
* /speciesAttack/\<int:pk> - Returns all information for the provided Species Attack.
* /trainer/\<int:pk> - Returns all information for the provided Trainer.
* /trainerAttack/\<int:pk> - Returns all information for the provided Trainer Attack.
* /trainerEdge/\<int:pk> - Returns all information for the provided Trainer Edge.
* /trainerFeature/\<int:pk> - Returns all information for the provided Trainer Feature.
* /generate/ - Returns a randomly generated Pokemon.
* /addItem/ - Creates a new Item entry in the DB.
* /addPokemonAttack/ - Creates a new Pokemon Attack entry in the DB.
* /addTrainerAttack/ - Creates a new Trainer Attack entry in the DB.
* /addTrainerEdge/ - Creates a new Trainer Edge entry in the DB.
* /addTrainerFeature/ - Creates a new Trainer Feature entry in the DB.

# Lint/Unit Testing
## Linting
- `npm run lint` -> general format/style checking.
- `npm run lint:pretty` -> automatically fix the format/style.

# --------------------

# Version(s)
- project: 1.0.0

# Update(s)
- Project(s): 04/2020
- README(S): 04/2020
