# PROJECT ADONISJS API MAIN BERSAMA 
- Author : Rully Afrizal Alwin
- Link Deployment : https://api-sb23-adonis.herokuapp.com/

## API endpoints

  #### Usage 
- https://api-sb23-adonis.herokuapp.com/{endpoint route}

  ### VENUES
| Route  | HTTP Method | Middleware  | Handler |
| ------------- | ------------- | ------------- | ------------- |
| /api/v1/venues  | GET  | auth,verify,role:user,venue_owner  | VenuesController.index  |
| /api/v1/venues  | POST  | auth,verify,role:venue_owner  | VenuesController.store  |
| /api/v1/venues/:id  | GET  | auth,verify,role:user,venue_owner  | VenuesController.show  |
| /api/v1/venues/:id  | PUT  | auth,verify,role:venue_owner  | VenuesController.update  |
| /api/v1/venues/:id  | DELETE  | auth,verify,role:venue_owner  | VenuesController.destroy  |

  ### FIELDS
| Route  | HTTP Method | Middleware  | Handler |
| ------------- | ------------- | ------------- | ------------- |
| /api/v1/venues/:venue_id/fields  | GET  | auth,verify,role:user,venue_owner  | FieldsController.index  |
| /api/v1/venues/:venue_id/fields  | POST  | auth,verify,role:venue_owner  | FieldsController.store  |
| /api/v1/venues/:venue_id/fields/:id  | GET  | auth,verify,role:user,venue_owner  | FieldsController.show  |
| /api/v1/venues/:venue_id/fields/:id  | PUT  | auth,verify,role:venue_owner  | FieldsController.update  |
| /api/v1/venues/:venue_id/fields/:id   | DELETE  | auth,verify,role:venue_owner  | FieldsController.destroy  |

   ### BOOKINGS
| Route  | HTTP Method | Middleware  | Handler |
| ------------- | ------------- | ------------- | ------------- |
| /api/v1/venues/:venue_id/bookings   | GET  | auth,verify,role:user,venue_owner  | BookingsController.index  |
| /api/v1/venues/:venue_id/bookings   | POST | auth,verify,role:user  | BookingsController.store  |
| /api/v1/venues/:venue_id/bookings/:id   | GET  |  auth,verify,role:user,venue_owner  | BookingsController.show  |
| /api/v1/venues/:venue_id/bookings/:id  | PUT  | auth,verify,role:user  | BookingsController.update  |
| /api/v1/venues/:venue_id/bookings/:id  | DELETE  | auth,verify,role:user  | BookingsController.destroy  |
| /api/v1/bookings/:id/join   | POST  | auth,verify,role:user  | BookingsController.joinBooking  |
| /api/v1/bookings/:id/unjoin   | POST  | auth,verify,role:user  | BookingsController.unjoinBooking  |
| /api/v1/bookings/schedules  | GET  | auth,verify,role:user  | BookingsController.schedules  |

   ### AUTHENTICATION
| Route  | HTTP Method | Middleware  | Handler |
| ------------- | ------------- | ------------- | ------------- |
| /api/v1/register  | POST  |   | AuthController.register  |
| /api/v1/verification  | POST  |   | AuthController.verification  |
| /api/v1/regenerate-otp  | POST  |   | AuthController.regenerateOtp  |
| /api/v1/login  | POST  | verify  | AuthController.login  |


# TERIMA KASIH
