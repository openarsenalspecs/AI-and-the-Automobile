# TerraRoam

## Safe Paths. Wild Places.

TerraRoam is an open-source, AI-powered travel intelligence platform designed to combine navigation, vehicle-aware routing, camping and overnight discovery, activities and attractions, verified travel reviews, trip planning, and real-time AI assistance into a unified travel system.

TerraRoam is designed for travelers using cars, vans, RVs, trailers, trucks, and other vehicles with physical dimensions or routing requirements that ordinary navigation systems may not adequately consider.

The platform is designed as a **modular, extensible, self-hostable architecture**. Essential functionality belongs in the TerraRoam Core, while specialized functionality can be added through optional plugin modules without requiring changes to the core platform.

TerraRoam is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.

---

## Project Vision

TerraRoam is intended to become a comprehensive travel intelligence system rather than simply another navigation application.

The platform should help users answer questions such as:

- What is the safest route for my specific vehicle?
- Can my RV or trailer physically navigate this road?
- Where can I safely stop for fuel, food, rest, or overnight camping?
- What scenic locations are near my route?
- What museums, attractions, historical sites, trails, or activities should I visit?
- Is there a better route because of weather, terrain, road restrictions, or closures?
- What destinations fit my interests and available travel time?
- What have other verified travelers experienced at a location?
- What should I know before entering an unfamiliar area?
- What should I download before entering an area without cellular service?

The long-term goal is to create a system that understands the relationship between the traveler, vehicle, road, destination, environment, and journey.

---

# Core Architecture

TerraRoam must use a modular architecture in which core capabilities are separated into independent modules with defined interfaces.

The architecture should allow individual components to be:

- Developed independently
- Tested independently
- Updated independently
- Replaced independently
- Scaled independently
- Disabled when unnecessary
- Extended through plugins

Core modules must not depend directly on optional plugins.

Plugins must communicate with TerraRoam through documented APIs, events, extension points, and permission-controlled interfaces.

---

# Core Modules

## 1. Mapping & Geospatial Core

The Mapping & Geospatial Core provides the geographic foundation for TerraRoam.

### Responsibilities

- Interactive maps
- GPS positioning
- Geospatial queries
- Road network representation
- Points of interest
- Terrain information
- Elevation data
- Map layers
- Geographic boundaries
- Coordinate conversion
- Geospatial indexing
- Map data synchronization
- Offline map regions

### Mapping Requirements

The architecture should support:

- OpenStreetMap data
- Vector maps
- Raster map layers
- Satellite imagery integrations
- Terrain layers
- Topographic layers
- Elevation datasets
- Public geographic datasets

Map providers must be abstracted behind provider interfaces so the application is not permanently tied to a single mapping provider.

---

## 2. GPS & Navigation Core

The GPS & Navigation Core manages the user's current position and navigation state.

### Responsibilities

- GPS location acquisition
- Position tracking
- Route progress
- Turn-by-turn navigation
- Navigation instructions
- Off-route detection
- Route recalculation
- Location accuracy monitoring
- Background navigation
- Heading and direction information

The system should be designed to support available positioning technologies and should not assume that GPS is the only positioning source.

---

## 3. Vehicle Profile Core

The Vehicle Profile Core stores the physical and operational characteristics required for vehicle-aware travel.

### Vehicle Attributes

Users should be able to define:

- Vehicle type
- Height
- Width
- Length
- Weight
- Gross vehicle weight
- Axle configuration
- Number of axles
- Trailer presence
- Trailer dimensions
- Trailer weight
- Fuel type
- Fuel capacity
- Estimated fuel economy
- EV battery capacity
- EV range
- Preferred fuel or charging networks

Vehicle profiles should support multiple vehicles per account.

Users should be able to select a vehicle profile before creating or starting a trip.

---

## 4. Vehicle-Aware Routing Core

The Vehicle-Aware Routing Core is one of TerraRoam's primary differentiating capabilities.

Routing must consider the physical characteristics of the selected vehicle.

### Routing Constraints

The engine should evaluate available data for:

- Low bridges
- Height restrictions
- Width restrictions
- Weight restrictions
- Length restrictions
- Vehicle restrictions
- Road classifications
- Truck restrictions
- Trailer restrictions
- Steep grades
- Sharp turns
- Narrow roads
- Difficult terrain
- Surface types
- Seasonal road closures
- Road access restrictions

The system must distinguish between:

- Confirmed restrictions
- Probable restrictions
- Unknown restrictions
- User-reported restrictions

Unknown information must not be silently treated as safe.

### Route Modes

The core routing system should support:

- Safest Route
- Efficient Route
- Scenic Route
- Low-Stress Route
- Adventure Route

Routing priorities must be configurable while maintaining safety constraints.

Safety constraints must override user preferences when a route violates known vehicle limitations.

---

## 5. Trip Planning Core

The Trip Planning Core manages multi-stop journeys.

### Responsibilities

- Trip creation
- Multiple destinations
- Waypoints
- Day-by-day planning
- Route sequencing
- Estimated travel times
- Stop planning
- Overnight planning
- Saved trips
- Trip duplication
- Trip sharing
- Collaborative planning
- Route modifications

Users should be able to create trips manually or ask the AI system to generate an initial itinerary.

---

## 6. Camping & Overnight Core

The Camping & Overnight Core manages overnight travel locations.

### Supported Location Types

- Campgrounds
- RV parks
- Public campgrounds
- Private campgrounds
- Dispersed camping areas
- Boondocking locations
- Farm stays
- Glamping
- Cabins
- Rest areas where overnight stays are permitted
- Truck stops
- Other legally available overnight locations

### Location Data

Listings may contain:

- Location
- Legal status
- Operating season
- Maximum vehicle length
- Maximum vehicle height
- Maximum vehicle width
- Hookups
- Electricity
- Water
- Sewer
- Dump facilities
- Surface type
- Road access
- Cell signal information
- Noise information
- Pet policies
- Accessibility information
- Fire restrictions
- Amenities
- Reservation information
- User reports

The system must distinguish verified data from community-reported information.

---

## 7. Activities & Discovery Core

The Activities & Discovery Core provides destination discovery beyond navigation.

### Supported Destinations

- Museums
- Historical sites
- Scenic viewpoints
- Parks
- Trails
- Beaches
- Natural attractions
- Cultural attractions
- Local attractions
- Restaurants
- Markets
- Festivals
- Tours
- Events
- Recreational activities
- Educational attractions
- Photography locations
- Points of interest

### Discovery Filters

Users should be able to filter recommendations by:

- Distance
- Travel time
- Cost
- Duration
- Accessibility
- Pet friendliness
- Family suitability
- Indoor or outdoor
- Interest category
- Opening hours
- Seasonal availability

---

## 8. AI Recommendation Core

The AI Recommendation Core converts TerraRoam's geographic, travel, vehicle, and user information into recommendations.

### AI Inputs

The recommendation system may consider:

- Current location
- Destination
- Vehicle profile
- Trip objectives
- Route
- Weather
- Terrain
- Road conditions
- Travel time
- Available daylight
- Interests
- Saved destinations
- Previous trips
- Living Route Memory
- Camping preferences
- Activity preferences

### AI Outputs

The system may recommend:

- Routes
- Scenic detours
- Campgrounds
- Overnight locations
- Attractions
- Museums
- Restaurants
- Fuel stops
- EV charging locations
- Rest stops
- Activities
- Alternative destinations
- Travel schedules
- Departure times

AI recommendations must provide meaningful reasoning when practical.

---

## 9. Living Route Memory Core

Living Route Memory provides user-controlled travel memory.

It allows TerraRoam to learn from previous trips without requiring users to repeatedly provide the same preferences.

### Capabilities

- Previously traveled routes
- Favorite destinations
- Saved locations
- Skipped locations
- Frequently visited areas
- Preferred camping styles
- Scenic preferences
- Traffic preferences
- Road-type preferences
- Travel pace
- Typical trip duration
- Preferred stop frequency

### Personal Route Profile

The system may develop a user-specific profile containing preferences such as:

- Scenic versus efficient travel
- Traffic avoidance
- Highway preference
- Rural road preference
- Dirt-road tolerance
- Camping preferences
- Activity preferences
- Driving comfort preferences

### Privacy Requirements

Living Route Memory must be:

- Opt-in where appropriate
- User-controlled
- Exportable
- Deletable
- Transparent
- Protected from unauthorized access

TerraRoam must never treat personal travel memory as property of the platform.

---

## 10. AI Co-Pilot Core

AI Co-Pilot provides conversational assistance during trip planning and navigation.

### Capabilities

Users should be able to ask questions such as:

- "Where should I stop next?"
- "Find a campground before sunset."
- "Is there a safer route?"
- "Is there anything interesting nearby?"
- "Find a museum along my route."
- "Where can I fuel this vehicle?"
- "Find a scenic detour that adds less than an hour."
- "Plan a five-day scenic RV trip."
- "Should I reroute because of the weather?"

### Voice Interaction

The architecture should support:

- Speech recognition
- Natural language understanding
- Spoken responses
- Hands-free interaction
- Navigation-aware conversation

### Driving Mode

Driving mode should prioritize safety.

The interface should:

- Minimize visual interaction
- Favor voice interaction
- Suppress unnecessary notifications
- Provide simple confirmations
- Prioritize critical alerts

AI Co-Pilot must never override vehicle safety constraints merely because a user requests a faster route.

---

## 11. Verified Review & Trust Core

TerraRoam should provide a review system designed to reduce fraudulent or misleading reviews.

### Verification Methods

The system may verify experiences through:

- Booking records
- Payment records
- Receipts
- Reservation confirmations
- Partner APIs
- Verified check-ins
- Other approved proof-of-visit mechanisms

### Review Features

- Verified reviewer status
- Verified stay indicators
- Verified purchase indicators
- Photo reviews
- Video reviews
- Category ratings
- Review history
- Reviewer reputation
- Fraud detection
- Suspicious activity reporting

The platform should preserve a distinction between verified experiences and unverified community information.

---

## 12. Safety & Hazard Core

The Safety & Hazard Core provides travel safety information.

### Potential Data Sources

- Road closures
- Weather conditions
- Flooding
- Wildfire activity
- Severe storms
- High winds
- Snow and ice
- Landslide information
- Construction
- Road restrictions
- Wildlife crossing information
- Other public safety datasets

### Safety Rules

Safety information must include data provenance and timestamps whenever available.

Stale or uncertain information should be identified as such.

TerraRoam should never represent an uncertain safety prediction as a guaranteed fact.

---

## 13. Offline Core

TerraRoam must be designed for travel environments where connectivity cannot be assumed.

### Offline Capabilities

- Downloadable maps
- Saved routes
- Cached destinations
- Cached campground information
- Cached points of interest
- Cached emergency information
- Offline trip plans
- Offline navigation support where supported by the routing architecture

The application should detect upcoming connectivity gaps and allow users to download relevant data before entering them.

---

## 14. Data Ingestion Core

The Data Ingestion Core provides standardized ingestion of external geographic and travel information.

### Responsibilities

- Import geographic data
- Import road data
- Import POI data
- Import campground data
- Import activity data
- Import public safety data
- Normalize external datasets
- Validate incoming data
- Track data provenance
- Detect conflicting records
- Manage data freshness

Every external dataset should be represented through a provider abstraction.

TerraRoam should avoid hard-coding business logic around a single external provider.

---

## 15. Search Core

The Search Core provides unified search across TerraRoam data.

Users should be able to search for:

- Locations
- Addresses
- Campgrounds
- Attractions
- Activities
- Restaurants
- Scenic locations
- Routes
- Trips
- Saved locations

Search should support:

- Geographic proximity
- Categories
- Natural-language queries
- Vehicle compatibility
- User preferences
- Availability where supported

---

## 16. User, Identity & Privacy Core

The identity system manages users and permissions.

### Requirements

- Account management
- Authentication
- Authorization
- User profiles
- Vehicle profiles
- Saved trips
- Saved locations
- Privacy controls
- Data export
- Data deletion
- Location-sharing controls

Sensitive information must be minimized and protected.

---

# Optional Plugin Modules

Optional plugins extend TerraRoam without increasing the dependency requirements of the core system.

Plugins must be independently installable and removable.

## 1. Weather Intelligence Plugin

Potential capabilities:

- Forecast integration
- Severe weather alerts
- Weather-aware routing
- Wind alerts
- Temperature alerts
- Storm tracking
- Precipitation forecasting
- Weather-based campground recommendations

---

## 2. Fuel & Energy Plugin

Potential capabilities:

- Fuel station discovery
- Fuel price information
- Fuel range calculations
- Fuel stop optimization
- EV charger discovery
- Charging route optimization
- Charging availability
- Charging-network integrations

---

## 3. Advanced EV Plugin

Potential capabilities:

- Battery-aware routing
- Battery consumption modeling
- Terrain-based range estimates
- Temperature-based range adjustments
- Charging-stop optimization
- Charger compatibility

---

## 4. Vehicle Diagnostics Plugin

Potential capabilities:

- OBD-II integration
- Vehicle telemetry
- Fuel efficiency monitoring
- Diagnostic code monitoring
- Tire information
- Engine data
- Battery information

Vehicle diagnostic integrations must be explicitly opt-in.

---

## 5. AR Exploration Plugin

Potential capabilities:

- Augmented reality navigation
- Landmark identification
- Scenic-point overlays
- Historical information
- Nearby attraction overlays
- Directional overlays

---

## 6. Stargazing & Night Sky Plugin

Potential capabilities:

- Dark-sky locations
- Light pollution maps
- Stargazing recommendations
- Meteor shower information
- Astronomical event alerts
- Night-sky conditions

---

## 7. Wildlife & Nature Plugin

Potential capabilities:

- Wildlife viewing locations
- Seasonal wildlife activity
- Migration information
- Wildlife crossing alerts
- Nature observations
- Conservation-area information

Wildlife information must never encourage unsafe interaction with animals.

---

## 8. Overlanding Plugin

Potential capabilities:

- Trail discovery
- Trail difficulty
- Surface information
- Terrain difficulty
- Recovery considerations
- Seasonal trail status
- Vehicle suitability

---

## 9. International Travel Plugin

Potential capabilities:

- International routing
- Country-specific road restrictions
- Vehicle regulations
- Border information
- Toll information
- Driving requirements
- Language support
- Regional map datasets

---

## 10. Emergency & Evacuation Plugin

Potential capabilities:

- Emergency route planning
- Evacuation route information
- Disaster-zone mapping
- Shelter information
- Emergency facility discovery
- Hazard-area avoidance

Emergency information must clearly identify its source and freshness.

---

## 11. Travel Booking Plugin

Potential capabilities:

- Campground reservations
- Hotel reservations
- Tours
- Activities
- Attraction tickets
- Experience bookings

Booking providers must be integrated through provider abstractions rather than embedded directly into core business logic.

---

## 12. Social & Group Travel Plugin

Potential capabilities:

- Shared trips
- Group itineraries
- Convoy mode
- Live group location sharing
- Group messaging
- Shared destinations
- Travel journals
- Community events

Location sharing must always be explicitly controlled by the user.

---

## 13. Advanced Review Intelligence Plugin

Potential capabilities:

- Review fraud detection
- Reviewer reputation analysis
- Sentiment analysis
- Review clustering
- Duplicate-review detection
- Anomaly detection
- Evidence analysis

---

## 14. Predictive Travel Intelligence Plugin

Potential capabilities:

- Predicted congestion
- Predicted campground demand
- Best departure time
- Seasonal travel intelligence
- Crowd forecasting
- Future road-risk analysis
- Predictive stop recommendations

Predictions must be clearly labeled as predictions rather than guaranteed conditions.

---

## 15. Community Mapping Plugin

Potential capabilities:

- User-submitted road conditions
- User-submitted campsite information
- Road hazard reports
- Trail reports
- Cell signal reports
- Surface condition reports
- Community corrections

Community information must maintain provenance, timestamps, confidence levels, and moderation controls.

---

# Plugin Architecture

Plugins should communicate with TerraRoam through documented interfaces.

The plugin architecture should support:

- Plugin discovery
- Plugin installation
- Plugin removal
- Plugin configuration
- Plugin permissions
- Plugin versioning
- Plugin dependency management
- Plugin isolation
- Plugin health monitoring
- Plugin API compatibility

A plugin must not be able to access user data or location information without explicit permission.

---

# Recommended Technology Stack

## Client Applications

Preferred architecture:

- Flutter for cross-platform mobile development
- Web application using a modern web framework where appropriate
- MapLibre for open-source map rendering
- Local SQLite-based storage for offline application data

The client architecture should separate:

- Presentation
- Navigation state
- Local storage
- Synchronization
- Mapping
- GPS
- API communication
- AI interaction

---

## Backend

Recommended primary backend:

- Python
- FastAPI
- PostgreSQL
- PostGIS
- Redis

The backend should use service boundaries that allow future components to be separated into independently scalable services.

---

## Geospatial Infrastructure

Recommended components:

- OpenStreetMap
- PostGIS
- MapLibre
- OSRM and/or GraphHopper
- Elevation datasets
- Terrain datasets

Routing engines must be abstracted so TerraRoam can support multiple routing implementations.

---

## AI Infrastructure

The AI layer should be provider-agnostic.

It should support:

- Hosted AI models
- Self-hosted models
- Local models
- Traditional machine learning
- Rules engines
- Recommendation models
- Geospatial models
- Retrieval-augmented generation

The AI architecture should allow models to be replaced without rewriting TerraRoam's core systems.

---

## Search Infrastructure

Recommended options include:

- PostgreSQL full-text search
- OpenSearch
- Vector search
- Geospatial search through PostGIS

Search providers should be abstracted behind a common TerraRoam search interface.

---

## Storage

Recommended storage architecture:

- PostgreSQL/PostGIS for structured and geospatial data
- S3-compatible object storage for images and documents
- MinIO for self-hosted object storage
- Local SQLite storage for offline client data

---

## Caching

Redis may be used for:

- Route caching
- Search caching
- Session state
- Temporary AI results
- Rate limiting
- Real-time application state

Cached information must have appropriate expiration and freshness policies.

---

# Data Provenance

TerraRoam must track the origin of important external information.

Where practical, records should contain:

- Source
- Source identifier
- Retrieval timestamp
- Last verification timestamp
- Data version
- Confidence level
- Modification history

Data provenance is particularly important for:

- Road restrictions
- Safety information
- Campground legality
- Weather information
- Reviews
- Community reports

---

# AI Governance

AI must assist the user without pretending to possess certainty where none exists.

The system must:

- Distinguish facts from predictions
- Provide confidence information where appropriate
- Identify uncertain data
- Preserve data provenance
- Avoid inventing destinations, restrictions, reviews, or services
- Avoid overriding confirmed safety constraints
- Respect user privacy
- Allow users to understand why major recommendations were made

Safety-critical decisions must have deterministic validation layers independent of generative AI.

Generative AI must not be the sole authority for vehicle clearance, legal access, road restrictions, emergency information, or other safety-critical routing decisions.

---

# Security Requirements

TerraRoam should implement:

- Secure authentication
- Role-based authorization where required
- Encryption in transit
- Encryption for sensitive stored information
- Secure credential management
- API authentication
- Rate limiting
- Audit logging
- Secure plugin permissions
- Dependency vulnerability scanning
- Secure update procedures

Secrets must never be committed to the repository.

---

# Privacy Requirements

TerraRoam should follow data minimization principles.

Users should control:

- Location history
- Living Route Memory
- Saved trips
- Vehicle profiles
- Shared locations
- Community contributions
- Reviews
- Personal preferences

Users should be able to export and delete applicable personal data.

TerraRoam should not sell personal location data.

---

# Development Principles

Contributors and AI development agents should follow these principles:

1. Build modules, not monoliths.
2. Prefer open-source technologies.
3. Avoid unnecessary vendor lock-in.
4. Use provider abstractions for external services.
5. Keep safety-critical logic deterministic and testable.
6. Treat external data as potentially incomplete or stale.
7. Preserve data provenance.
8. Design for offline operation.
9. Design for global expansion.
10. Make components replaceable.
11. Write automated tests for critical functionality.
12. Document public APIs and module interfaces.
13. Never introduce an undocumented dependency.
14. Never fabricate data, APIs, or capabilities.
15. Maintain compatibility wherever practical.

---

# Future Architecture Goals

TerraRoam should be capable of eventually supporting:

- International travel
- Autonomous vehicle systems
- Advanced EV routing
- Vehicle telemetry
- Augmented reality
- Predictive travel intelligence
- Advanced environmental intelligence
- Emergency evacuation intelligence
- Community-generated geospatial data
- New transportation modes
- New AI model architectures
- New mapping providers
- New routing engines

The architecture should be designed so these capabilities can be introduced primarily through modules or plugins rather than requiring a fundamental rewrite of the platform.

---

# Testing

Critical TerraRoam systems must have automated tests.

Testing should include:

- Unit testing
- Integration testing
- API testing
- Geospatial testing
- Routing testing
- Vehicle constraint testing
- Offline testing
- Synchronization testing
- AI evaluation
- Security testing
- Performance testing

Vehicle-aware routing must be tested against combinations of:

- Vehicle dimensions
- Trailer dimensions
- Road restrictions
- Bridge restrictions
- Weight restrictions
- Grade limitations
- Road classifications

---

# Self-Hosting

TerraRoam should be designed for self-hosted deployment.

The architecture should support:

- Local development
- Single-server deployment
- Containerized deployment
- Cloud deployment
- Private infrastructure
- Community-hosted instances

External services should be optional wherever practical.

---

# Open-Source Development

TerraRoam is intended to benefit from contributions from:

- Software developers
- AI engineers
- GIS specialists
- Transportation experts
- RV and overlanding communities
- Travelers
- Accessibility advocates
- Data engineers
- Security researchers
- Open-source contributors

Contributions should preserve TerraRoam's modular architecture and safety-first principles.  

---

# Vision

TerraRoam is designed to become a continuously evolving travel intelligence platform that understands not only where a traveler wants to go, but also how they travel, what their vehicle can safely handle, what is happening along the route, what they may want to experience, and what information they need before they arrive.

The core platform provides the foundation.

Plugins provide the expansion layer.

AI provides the intelligence layer.

Open-source development provides the evolution layer.

Together, these components are intended to make TerraRoam a comprehensive, adaptable, and user-controlled system for exploring the world.

**TerraRoam: Safe Paths. Wild Places.**

---

## Specification Branding License (SBL)
### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/terraroam/](https://roxanneardary.com/terraroam/)  

---


## 📦 License & Notice Requirements

TerraRoam is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- TerraRoam specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
