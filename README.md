# Welp


## Minimum Viable Product
This project is a clone of Yelp built on Rails and Backbone. Users can:

<!-- This is a Markdown checklist. Use it to keep track of your progress! -->

- [ ] Create accounts
- [ ] Create sessions (log in)
- [ ] Create restaurants with locations
- [ ] Create restaurant reviews
- [ ] View restaurants and reviews
- [ ] Search for restaurants by title
- [ ] Search for restaurants by location
- [ ] Have a newsfeed of activity.

## Design Docs
* [View Wireframes][views]
* [DB schema][schema]

[views]: ./docs/views.md
[schema]: ./docs/schema.md

## Implementation Timeline

### Phase 1: User Authentication, Restaurant and Review Creation (~1 day)
I will implement user authentication in Rails based on the practices learned at
App Academy. By the end of this phase, users will be able to create restaurants and reviews using
a simple text form in a Rails view. The most important part of this phase will
be pushing the app to Heroku and ensuring that everything works before moving on
to phase 2.

[Details][phase-one]

### Phase 2: Viewing Restaurants and Reviews (~2 days)
I will add API routes to serve restaurant and review data as JSON, then add Backbone
models and collections that fetch data from those routes. By the end of this
phase, users will be able to create blogs and view both blogs and posts, all
inside a single Backbone app.

[Details][phase-two]

### Phase 3: Editing and Displaying Reviews (~2 days)
I plan to use third-party libraries to add functionality to the `ReviewForm` and
`ReviewShow` views in this phase. I also plan to integrate Filepicker for file upload so
users can add images to reviews.

[Details][phase-three]

### Phase 4: User Feeds (~1-2 days)
I'll start by adding a `feed` route that uses the `current_user`'s
recent activity to serve a list of blog posts ordered
chronologically. On the Backbone side, I'll make a `FeedShow` view that pulls from the `current_user`'s recent activity.  Ultimately, this will be the page users
see after logging in.

[Details][phase-four]

### Phase 5: Searching for Restaurants (~2 days)
I'll need to add `search` routes to the Restaurants controller. On the
Backbone side, there will be a `SearchResults` composite view that has `RestaurantsIndex` subviews. These views will use a plain old `Restaurants`
collection, but they will fetch from the new `search` routes.

[Details][phase-five]

### Bonus Features (TBD)
- [ ] Lists of restaurants made by users
- [ ] A Google Maps view of all restaurants
- [ ] Pagination/infinite scroll
- [ ] A more complicated search by price, etc.
- [ ] User avatars
- [ ] Multiple sessions/session management
- [ ] Typeahead search bar

[phase-one]: ./docs/phases/phase1.md
[phase-two]: ./docs/phases/phase2.md
[phase-three]: ./docs/phases/phase3.md
[phase-four]: ./docs/phases/phase4.md
[phase-five]: ./docs/phases/phase5.md
