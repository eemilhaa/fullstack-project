# fullstack-project

This project is an interactive map UI that allows for exploring travel times in the Helsinki metropolitan region.

The frontend is live at https://traveltimematrix.rahtiapp.fi

## Description

### User-facing features
The user can hover their mouse on the map component in the UI, and the travel times shown on the map update in real-time.
If the user clicks on the map, the map locks on the clicked location and hovering produces an updating tooltip instead of map updates.
When clicked again, the map interaction goes back to hover mode.
In addition to location, the user can select from different travel modes for which the travel times are shown.

### Technologies
The frontend is developed with React. The backend is a configured nginx web server serving precompressed static content.
All development and production environments are containerized, production container builds are automated with github actions.
All deployments are done with kubernetes (openshift) and the current live version is running on csc rahti.
The frontend and backend are documented more in their respective repositories (readmes).

### Disclaimer
This work is part of a larger project (my msc thesis)
and utilizes a dataset made by Helsinki uni's Digital Geography Lab.
However, the entire development process documented in this repository is
done solely by me and with the fullstack project course in mind.

## Repositories

The frontend and backend are in separate repositories.
There is also a third repository holding all of the data preprocessing scripts.
Since that is not directly relevant to web-development,
I have not inlcuded it in the working hours,
and am not expecting it to be code-reviewed or in any way considered in grading.

- [Frontend](https://github.com/eemilhaa/travel-time-matrix-visualisation-frontend)
- [Backend](https://github.com/eemilhaa/travel-time-matrix-visualisation-backend)
- ([Data preprocessing](https://github.com/eemilhaa/travel-time-matrix-visualisation-preprocessing), **NOT included in working time**)

I would prefer for any code-reviews to be done in this repository,
or my forks (linked above)
since those are where all development has happened
and where any possible further development will happen.

## Hours spent (only the fullstack-relevant ones)
| Day | Hours spent | What I did |
|-|-|-|
| 27.6. | 3 | Frontend: Search tools for frontend setup, land on vite |
|       | 5 | Frontend: Experiment with integrating deck.gl and react, produce minimal working map application |
| 29.6. | 4 | Backend + Frontend: Study nginx for front / backend server |
| 30.6. | 5 | Frontend: Add interactive location picking, refactor map styling |
|       | 3 | Backend: Produce a working nginx config, containerize |
| 1.7. | 2 | Frontend: Consider feature scope, add initial documentation (readme), map styling |
| 3.7. | 5 | Frontend: Add components for travel mode buttons and top bar for hosting buttons |
| 20.8. - 21.8. | 3 | Backend: Make a nginx image containing custom config, automate build with github actions |
| 21.8. | 5 | Backend: Study kubernetes (and openshift) to deploy on rahti, produce minimal manifest file for deployment |
|       | 2 | Backend: Make container image non-root (required by openshift) |
| 22.8. | 4 | Backend: Study kubernetes more, add service for exposing deployment network |
|       | 1 | Backend: Debug container image |
| 23.8. | 5 | Backend: Study kubernetes (data persistence), add capabilities for persisting data in production, debug deployment |
| 24.8. | 6 | Backend: Make a persitent data volume that is available to all replicas in deployment |
|       | 1 | Backend: Small cleanup |
|       | 1 | Backend: Add documentation (readme) |
| 25.9. - 1.9. | 1 | Backend: Cleanup, tweak deployment, use gzip |
| 28.8. | 4 | Frontend: Containerize app for production |
|       | 1 | Frontend: Add github workflow for automating prod container build |
|       | 1 | Frontend: Add kubernetes deployment manifest |
| 2.9. | 2 | Frontend: Containerize development environment |
| 4.9. | 1 | Frontend: Set backend url dynamically |
| 8.9. | 1 | Frontend: Make containers better - set env vars, node version, install correct dependencies |
|      | 1 | Frontend: Troubleshoot improper map rendering in deck.gl |
| 9.9. | 5 | Frontend: Add separate hover / click modes |
| 11.9. | 1 | Frontend: Improve hover / click mode switching |
|       | 6 | Frontend: Switch mapping library to maplibre due to [deck.gl bug](https://github.com/visgl/deck.gl/issues/8107), reimplement with maplibre |
|       | 2 | Frontend: Deploy new implementation, do general project cleanup |
|       | 1 | Frontend: Add map controls, do initial styling |
| 13.9. | 1 | Frontend: Make minor adjustments to account for changes in data, update documentation (readme) |
|       | 1 | Backend: Debug data transfer to production, add rsync to backend image for moving data to rahti |
| 14.9. | 4 | Frontend + Backend: Study routes in kubernetes, switch routes in all deployments to use https instead of http |
|       | 3 | Frontend: Add dynamic marker to map when clicked |
| 15.9. | 4 | Frontend: Add dynamic tooltip to map when hovered |
|       | 2 | Frontend: Refactor top bar component |
| 16.9. | 2 | Frontend: Add control panel component for hosting menu bars |
| 17.9. | 2 | Frontend: Add map legend component |
|       | 2 | Frontend: Experiment with styling |
|       | 3 | Frontend: Realize the ridiculousness of the menu bar component, reimplement the same functionality using simple drop-downs instead |
| 21.9. - 22.9. | 2 | Frontend: Minor map adjustments, make route redirect http requests to https |
| 25.9. - 4.9. | 1 | Frontend: Minor map updates |
| 4.10. | 3 | Backend: General cleanup, study nginx and enable senging precompressed files |
| 5.10. | 3 | Frontend: General cleanup & formatting |
|      | 1 | Frontend: Small refactoring of components |
| 2.2. - 4.2 | 4 | Frontend: Cleanup code, fix dev container |
| 4.2 | 1 | Frontend & backend: update documentation (readmes) |

### Total hours: 121
