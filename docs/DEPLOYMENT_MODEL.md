# Deployment Model

IX-Bayanihan-HydroGrid is designed to scale in controlled stages.

The primary deployment is the **HydroGrid Lot**.

The system may later expand into multi-lot clusters and, if justified by measured evidence and local capacity, into **Level 2 HydroGrid Flood-Resilience Buildings**.

The deployment model is intentionally staged because flood infrastructure must be validated before it is scaled.

## Deployment Levels

IX-Bayanihan-HydroGrid defines three major deployment levels:

1. **Level 1: HydroGrid Lot**
2. **Level 1.5: HydroGrid Cluster**
3. **Level 2: HydroGrid Flood-Resilience Building**

Each level has different cost, permitting, capacity, maintenance, and engineering requirements.

The repo focuses on Level 1 because it is the fastest realistic path to evidence.

## Level 1: HydroGrid Lot

A HydroGrid Lot is a bounded flood-resilience installation placed near a known flood chokepoint.

It is the primary deployment form for this repository.

A HydroGrid Lot is not a single device. It is a site package.

A complete lot may include:

- pump pods;
- debris intake system;
- water-level sensors;
- flow meters;
- pressure sensors;
- pump-current monitoring;
- battery backup;
- solar support where feasible;
- generator or fuel-cell interface where permitted;
- communications gateway;
- local event logging;
- maintenance access;
- local status indicators;
- stakeholder handoff documentation.

The lot model is intended for a specific site, not an entire city.

## Why Start With a Lot

The HydroGrid Lot is the recommended first deployment because it is:

- easier to pilot;
- easier to inspect;
- easier to maintain;
- easier to power;
- easier to validate;
- easier to permit than a building;
- easier to compare against a baseline;
- easier to shut down if it fails;
- easier for partners to fund as a first test.

A lot-scale deployment can demonstrate whether the concept works before larger infrastructure is considered.

## HydroGrid Lot Target Sites

A HydroGrid Lot may be appropriate near:

- an underpass;
- a road sump;
- a low-lying street;
- an evacuation-center access road;
- a school access route;
- a clinic or hospital approach road;
- a barangay hall access point;
- a pump-station approach;
- a canal choke;
- a clogged drainage inlet;
- a culvert;
- a creek crossing;
- a trash-rack location;
- a coastal outfall;
- an estuary backflow point;
- a retention or detention basin edge.

A candidate site should be selected because it has a repeatable flood pain point and a realistic path to measured improvement.

## HydroGrid Lot Minimum Viable Configuration

A minimum serious HydroGrid Lot should include:

- one bounded flood chokepoint;
- one reviewed discharge path;
- one debris intake assembly;
- one pump pod or pump-support interface;
- one water-level sensing point;
- one flow measurement point;
- one backup power system for critical loads;
- one local event logging system;
- one communications path;
- one maintenance process;
- one validation plan;
- one responsible operator or maintenance owner.

If the system includes pumping, measured flow is required.

If the system lacks maintenance ownership, it is not ready for deployment.

## HydroGrid Lot Standard Configuration

A standard HydroGrid Lot may include:

- two to ten pump pods;
- one shared debris intake zone;
- removable debris baskets;
- intake clog detection;
- outlet blockage detection;
- water-level sensing upstream of intake;
- water-level sensing near discharge or downstream point where useful;
- rainfall sensing;
- flow totalization;
- pump current and voltage sensing;
- battery bank;
- solar canopy or small solar support;
- weatherproof control enclosure;
- LoRa or equivalent low-power local communications;
- LTE or wired gateway where available;
- offline event logging;
- local beacon or status light;
- operator checklist;
- spare pump and field service kit.

This configuration is appropriate for a controlled pilot at a high-value chokepoint.

## HydroGrid Lot High Configuration

A high-configuration HydroGrid Lot may include:

- pump-pod cluster;
- larger battery bank;
- stronger discharge manifold;
- redundant flow measurement;
- salinity sensing where backflow is relevant;
- turbidity sensing where debris or sediment load matters;
- vibration sensing for pump health;
- hydrophone-style sensing for cavitation or turbulence where justified;
- floating or canal-side sentinel node;
- solar canopy or floating solar connection;
- generator or fuel-cell-ready protected interface where permitted;
- expanded local communications;
- public-works dashboard export;
- maintenance staging area;
- blackbox-style event logging;
- operator training package.

This configuration is still site-bounded. It should not be described as a citywide flood solution.

## Level 1.5: HydroGrid Cluster

A HydroGrid Cluster is a group of HydroGrid Lots placed across related flood chokepoints.

A cluster may serve:

- a small drainage basin;
- a set of connected streets;
- an evacuation route;
- a pump-station catchment approach;
- a canal corridor;
- a flood-prone barangay zone;
- a coastal or estuary interface.

The purpose of a cluster is to coordinate multiple sites that fail together.

## HydroGrid Cluster Functions

A HydroGrid Cluster can support:

- shared communications gateway;
- shared maintenance crew routing;
- basin-level water-level comparison;
- pump-state comparison;
- clog detection across multiple inlets;
- backflow detection across several outfalls;
- coordinated event logging;
- shared backup power planning;
- post-event review across a wider area.

A cluster should be built only after at least one lot-scale configuration has been tested or reviewed in detail.

## HydroGrid Cluster Requirements

A HydroGrid Cluster requires:

- a drainage-area map;
- site ownership or access plan for each lot;
- discharge path for each pump-support site;
- communications plan;
- maintenance route;
- spare parts plan;
- operator dashboard;
- escalation procedure;
- data retention plan;
- public-works coordination;
- cluster-level validation criteria.

A cluster without public-works coordination is likely to fail operationally.

## Level 2: HydroGrid Flood-Resilience Building

A HydroGrid Flood-Resilience Building is a future higher-capacity upgrade path.

It is not the first recommended deployment.

A Level 2 building is a purpose-built vertical flood-control utility node.

It may include:

- intake screening at lower levels;
- pump galleries;
- debris handling equipment;
- protected upper-level batteries;
- protected power electronics;
- backup energy systems;
- water-treatment support;
- maintenance shop;
- spare-parts storage;
- command room;
- communications mast;
- event logging systems;
- public-works dashboard operations;
- multi-site flood-state classification.

The building-scale concept exists because some flood pain points may eventually require more capacity than a lot-scale pilot can provide.

## Why the Building Path Matters

The building path matters because larger flood basins may need:

- more pump capacity;
- more battery capacity;
- better protection from floodwater;
- larger maintenance staging;
- command operations;
- backup energy;
- multi-site sensor integration;
- protected communications;
- long-term permanent infrastructure.

A Level 2 building may matter enough to justify future investment if Level 1 or Level 1.5 deployments produce evidence of value.

## Why the Building Is Not First

The building is not first because it requires:

- land acquisition or site control;
- major civil-engineering review;
- structural engineering;
- hydraulic analysis;
- electrical design;
- fire-safety review;
- environmental review;
- public-space approval;
- building permits;
- utility coordination;
- long-term staffing;
- long-term maintenance budget;
- large capital investment.

Without measured pilot evidence, a building-scale proposal may be too expensive and speculative for adoption.

The lot proves whether the building deserves to exist.

## Deployment Scaling Path

The recommended scaling path is:

```
Bench test
  -> Controlled wet test
      -> Single HydroGrid Lot
          -> Multi-lot HydroGrid Cluster
              -> Level 2 HydroGrid Flood-Resilience Building
```
A deployment should not jump directly to building scale unless a qualified public agency or engineering partner has already completed the required planning and review.

Stage 0: Concept Review

Before any build, partners should review:

project scope;
non-claims;
site-selection guide;
bill of materials;
safety and permitting requirements;
failure modes;
maintenance model;
validation plan.

The goal is to decide whether the architecture is worth evaluating for a real site.

Stage 1: Bench Test

A bench test is conducted away from public flood conditions.

It may test:

sensor readings;
local logging;
controller behavior;
pump control logic without public deployment;
battery monitoring;
communications;
event schema;
maintenance log format.

The bench test does not prove flood benefit.

It only verifies basic subsystem operation.

Stage 2: Controlled Wet Test

A controlled wet test uses a known water source and a safe discharge path.

It may test:

pump flow;
flow meter accuracy;
water-level sensing;
clog simulation;
outlet restriction simulation;
power draw;
battery runtime;
local logging;
alert behavior;
safe shutdown.

A controlled wet test is required before any claim of pump-support readiness.

Stage 3: Single HydroGrid Lot Pilot

A single HydroGrid Lot pilot tests the architecture at one selected flood chokepoint.

A pilot should define:

site boundary;
flood pain point;
expected water source;
approved discharge path;
installed modules;
maintenance owner;
safety reviewer;
operating procedure;
acceptance criteria;
failure criteria;
data collection plan.

A single-site pilot should not be described as proof of citywide effectiveness.

Stage 4: Multi-Lot Cluster

A multi-lot cluster tests coordinated operation across related chokepoints.

A cluster should define:

drainage relationship between lots;
shared communications;
maintenance route;
shared dashboard;
event comparison logic;
cluster-level failure criteria;
operator workflow;
expansion conditions.

Cluster scaling should occur only after single-lot lessons are incorporated.

Stage 5: Level 2 Building

A Level 2 building is a permanent infrastructure project.

Before building-scale deployment, partners must complete:

full site study;
civil engineering;
hydraulic modeling;
structural design;
fire-safety design;
electrical design;
environmental review;
public consultation where required;
permitting;
operations plan;
maintenance budget;
procurement plan.

The repository does not provide final building plans.

It provides the conceptual upgrade path and system logic.

Deployment Decision Rules

A deployment should proceed only if:

a real flood chokepoint is identified;
the discharge path is known;
maintenance ownership is assigned;
safety review is planned;
local authority review is possible;
system claims are bounded;
success criteria are measurable;
failure criteria are accepted;
budget includes maintenance and replacement parts.

A deployment should not proceed if:

there is no discharge path;
the site cannot be accessed safely;
maintenance ownership is absent;
public authority approval is unavailable;
operators cannot respond to alerts;
electrical safety cannot be assured;
claims depend on unvalidated assumptions;
the project is being presented as flood-proofing.
Deployment Roles

A serious deployment may require the following roles:

site owner;
public-works authority;
disaster-risk office;
civil engineer;
hydraulic engineer;
electrical engineer;
environmental reviewer;
safety reviewer;
maintenance crew;
operator;
data reviewer;
procurement owner;
community liaison.

The repository does not replace any of these roles.

Lot Deployment Footprint

A HydroGrid Lot footprint depends on configuration.

A small proof-of-concept may fit in a compact service area.

A serious pilot may require space for:

intake access;
pump access;
control enclosure;
battery enclosure;
solar support;
discharge line;
maintenance staging;
safe public separation;
spare parts;
service walkway.

No footprint should be finalized without site review.

Building Deployment Footprint

A HydroGrid Flood-Resilience Building footprint depends on capacity.

The building form should be treated as a utility facility, not a decorative tower.

It may require:

intake apron;
pump gallery;
discharge manifold;
electrical rooms;
battery rooms;
maintenance floors;
command room;
communications mast;
exterior equipment yard;
safe access;
emergency vehicle access;
flood-safe entry;
code-compliant energy storage areas.

Hydrogen or fuel-cell systems, if included, require additional safety separation and professional review.

Deployment Output

Every deployment stage should produce a reviewable output.

Bench Test Output
subsystem test notes;
sensor readings;
log format;
issues found;
changes required.
Controlled Wet Test Output
measured flow;
pump power draw;
clog simulation behavior;
outlet restriction behavior;
battery runtime;
event log completeness.
Single Lot Pilot Output
site description;
installed modules;
operating period;
flood event records;
maintenance records;
measured volume moved;
alerts issued;
failures observed;
pass/fail evaluation.
Cluster Output
multi-site event timeline;
site-to-site comparison;
maintenance routing result;
communications performance;
cluster-level lessons.
Building Planning Output
feasibility report;
hydraulic study;
engineering scope;
permitting path;
cost and maintenance estimate;
risk review.
Deployment Metrics

Useful deployment metrics include:

water-level detection accuracy;
time to alert;
flow rate;
total volume moved;
pump runtime;
pump energy use;
battery runtime;
communications uptime;
local log completeness;
clog detection accuracy;
outlet blockage detection accuracy;
maintenance response time;
flood duration at the chokepoint;
operator comprehension;
false alarm rate;
post-event review quality.

Metrics should be selected before deployment.

Deployment Failure Criteria

A deployment should be considered unsuccessful or not ready for expansion if:

measured flow is far below target;
intakes clog faster than they can be serviced;
operators cannot interpret alerts;
logs are incomplete;
power runtime is insufficient;
sensors drift without detection;
maintenance does not occur;
discharge path creates downstream risk;
public access becomes unsafe;
system claims exceed evidence.

Failure criteria are required to prevent false confidence.

Deployment Ethics

The system should be deployed only where it can be maintained, inspected, and reviewed.

It should not be placed in public space without approval.

It should not create hidden hazards.

It should not move water into another community without review.

It should not be advertised as protection it cannot provide.

It should not collect unnecessary personal data.

It should not use defense or disabling functions.

Recommended First Deployment

The recommended first deployment is:
```
One HydroGrid Lot
One known chokepoint
One valid discharge path
One pump-support module
One debris intake system
One water-level sensor
One flow meter
One battery-backed controller
One local event log
One maintenance owner
One validation plan
```
This first deployment gives partners a measurable starting point.

Summary

IX-Bayanihan-HydroGrid should be deployed in stages.

The lot is the practical first form.

The cluster is the district-scale coordination form.

The building is the future high-capacity municipal upgrade path.

Each stage should be justified by measured evidence, not by promises.

The system should scale only when the previous level proves value, exposes failure modes, and produces enough data for qualified partners to decide what comes next.
