# System Architecture

IX-Bayanihan-HydroGrid is a modular flood-resilience reference architecture.

The system is centered on the **HydroGrid Lot**: a bounded installation placed near a known flood chokepoint to support flood sensing, pump assistance, backup power, debris-aware maintenance, event logging, and public-works handoff.

The architecture is designed to be reviewed, tested, adapted, and validated by qualified partners before any real deployment.

It is not a certified flood-control product and not a construction-ready design.

## Architecture Summary

IX-Bayanihan-HydroGrid combines six major layers:

1. **Hydraulic Action Layer**
2. **Debris and Intake Layer**
3. **Sensing Layer**
4. **Power Resilience Layer**
5. **Communications and Logging Layer**
6. **Operations and Maintenance Layer**

Optional site-specific layers may include:

7. **Littoral Sentinel Layer**
8. **Renewable Energy Support Layer**
9. **Level 2 Building Upgrade Layer**

The system is intentionally modular so a partner can begin with a bounded pilot and expand only after measured evidence supports expansion.

## Primary System Boundary

The default system boundary is one HydroGrid Lot serving one selected flood chokepoint or a small cluster of nearby chokepoints.

A HydroGrid Lot may interface with:

- a flooded street low point;
- a curb inlet;
- a drain inlet;
- a culvert;
- a canal edge;
- a pump-station approach;
- a school, clinic, evacuation-center, or barangay access road;
- a coastal outfall;
- an estuary backflow zone;
- a retention basin;
- an approved discharge path.

The system boundary must include both the water source and the water destination.

A HydroGrid Lot cannot be evaluated honestly unless the discharge path is known.

## Architecture Principle 1: Water Must Go Somewhere

IX-Bayanihan-HydroGrid does not delete floodwater.

If pump support is used, water must be moved to a valid receiving location.

Possible receiving paths include:

- existing storm drain;
- canal;
- culvert;
- outfall;
- pump-station intake;
- retention basin;
- detention basin;
- swale;
- temporary bladder storage;
- approved transfer route.

The receiving path must be reviewed for legality, hydraulic capacity, backflow risk, contamination risk, and downstream impact.

Pumping without a valid receiving path can move the problem rather than reduce it.

## Architecture Principle 2: Pump Running Is Not Proof of Water Moved

A powered pump is not evidence of flood relief.

The architecture requires measured flow wherever pump support is claimed.

Evidence should include:

- flow rate;
- totalized volume;
- pump runtime;
- pump electrical load;
- intake water level;
- outlet pressure where relevant;
- rainfall context;
- maintenance events;
- clog or blockage indicators.

A system should not claim flood reduction from pumping unless measured flow and site response support that claim.

## Architecture Principle 3: Debris Is a Primary Failure Mode

Floodwater often carries debris.

Debris can include:

- plastic bags;
- bottles;
- leaves;
- branches;
- mud;
- sediment;
- trash;
- vegetation;
- floating waste;
- construction debris;
- mixed urban refuse.

The system must assume that intakes, screens, baskets, pumps, and outlets can clog.

The architecture includes debris-aware intake design, serviceable baskets, clog detection, flow verification, and maintenance logging.

A HydroGrid Lot without a maintenance plan is not a serious deployment.

## Architecture Principle 4: Critical Functions Need Backup Power

Flood events can coincide with unstable power.

The system should preserve critical functions during grid instability where feasible.

Critical functions may include:

- water-level sensing;
- pump control;
- pump operation where configured;
- local warning indicators;
- communications;
- event logging;
- battery monitoring;
- maintenance alerts.

Backup power does not mean unlimited operation.

The architecture requires defined runtime targets, load prioritization, and energy-use logging.

## Architecture Principle 5: No Single Sensor Should Declare a Major Failure

Flood-state classification should use confidence-gated logic.

A single reading may be wrong because of sensor drift, obstruction, electrical noise, installation error, debris, or local turbulence.

A better classification compares multiple signals.

For example:

- rising water level;
- pump current;
- measured flow;
- outlet pressure;
- rainfall intensity;
- vibration;
- salinity where relevant;
- neighboring node behavior;
- maintenance status.

The goal is to reduce false confidence and support better operator decisions.

## Architecture Principle 6: The First Product Is Evidence

The first useful output of a HydroGrid system is not a dramatic claim.

The first useful output is evidence.

Useful evidence includes:

- when flooding began;
- how fast water rose;
- when pumps activated;
- whether water moved;
- when clogging occurred;
- whether backflow indicators appeared;
- when power changed state;
- when communications failed or recovered;
- when maintenance occurred;
- how long water remained above a threshold.

Evidence makes the system reviewable.

## System Overview

```
Rainfall / runoff / backflow / local ponding
                |
                v
        Flood chokepoint
                |
                v
     Debris intake and screening
                |
                v
        Pump pod or monitored drain
                |
                v
        Valid discharge path
                |
                v
       Flow verification and logging
```

Parallel support layers:
- water-level sensing
- rainfall sensing
- pump-health sensing
- power backup
- communications
- local alerts
- maintenance workflow
- event blackbox logging

Layer 1: Hydraulic Action Layer

The Hydraulic Action Layer is responsible for moving or verifying water movement.

It may include:

dirty-water pump pods;
pump manifolds;
intake sumps;
discharge hoses or pipes;
check valves;
anti-backflow components;
flow meters;
outlet pressure sensors;
pump-current monitoring;
pump-health monitoring;
manual override controls.

The hydraulic layer is site-specific.

A small proof-of-concept may use one pump pod.

A larger pilot may use a cluster of pump pods.

A municipal installation may support multiple pump clusters or interface with existing pumping stations.

Hydraulic Action Layer Requirements

The hydraulic layer must define:

target flow rate;
expected head;
discharge route;
expected debris load;
pump duty cycle;
power requirement;
failure behavior;
safe shutdown behavior;
maintenance access;
measurement method.
Hydraulic Action Layer Non-Claims

The hydraulic layer does not guarantee flood reduction unless validated at the site.

Pump capacity must be compared against site runoff, receiving-path capacity, and actual measured performance.

Layer 2: Debris and Intake Layer

The Debris and Intake Layer protects the hydraulic system from clogging and supports maintenance.

It may include:

curb-mouth intake structure;
sloped screen;
trash rack;
removable debris basket;
sediment trap;
floating debris deflector;
coarse pre-screen;
optional rotating brush;
optional backflush function;
inspection access;
maintenance indicator.
Debris and Intake Layer Requirements

The intake layer must be serviceable.

A design that cannot be cleared safely during or after a flood event is not acceptable for serious deployment.

The intake layer should support:

fast visual inspection;
safe debris removal;
logged maintenance events;
clog detection;
continued partial operation where possible.
Debris and Intake Layer Non-Claims

The system does not claim debris immunity.

It aims to make debris failure visible, serviceable, and less likely to silently disable pumping.

Layer 3: Sensing Layer

The Sensing Layer measures flood and equipment state.

Candidate sensors include:

water-level sensor;
rainfall sensor;
flow meter;
pressure sensor;
pump-current sensor;
battery-voltage sensor;
battery-current sensor;
vibration sensor;
temperature sensor;
humidity sensor inside enclosures;
enclosure leak sensor;
salinity sensor where backflow is relevant;
turbidity sensor where sediment/debris load matters;
tilt sensor for floating or waterborne nodes;
acoustic or hydrophone-style sensor for pump cavitation or debris interaction where justified.

Sensors should be selected based on the site’s failure modes.

A dry inland underpass does not need the same sensor stack as a coastal outfall.

Sensing Layer Requirements

The sensing layer must support:

calibration procedure;
sensor health check;
timestamped readings;
local logging;
failure detection;
maintenance access;
replacement path.
Sensing Layer Non-Claims

Sensors do not control flooding by themselves.

Sensors provide evidence that can support action.

Layer 4: Power Resilience Layer

The Power Resilience Layer supports operation during grid instability.

It may include:

LiFePO4 battery bank;
solar support;
charge controller;
DC bus;
fuses;
breakers;
contactors;
battery management system;
current shunt;
power meter;
generator input where permitted;
fuel-cell input where professionally reviewed and approved;
supercapacitor buffer for low-power sensor or radio bursts;
load-priority controller.

The power layer should separate critical loads from optional loads.

Critical Loads

Critical loads may include:

water-level sensing;
event logging;
communications;
local status indicator;
control electronics;
selected pump operation where configured.
Optional Loads

Optional loads may include:

lighting beyond safety needs;
auxiliary charging;
research modules;
nonessential displays;
noncritical cameras.
Power Resilience Layer Requirements

The power layer must define:

battery capacity;
expected runtime;
load list;
charge sources;
safe shutdown thresholds;
enclosure protection;
grounding and bonding approach;
electrical safety review requirement;
maintenance interval.
Power Resilience Layer Non-Claims

Solar support does not guarantee storm operation.

Hydrogen or fuel-cell support, if included, is backup energy only and requires certified equipment, code compliance, and professional review.

The system does not use hydrogen to remove floodwater.

Layer 5: Communications and Logging Layer

The Communications and Logging Layer moves data to operators and preserves records if the network fails.

It may include:

LoRa node;
LoRaWAN gateway;
LTE router;
local Wi-Fi maintenance access;
wired maintenance port;
SD card or industrial local storage;
dashboard export;
status beacon;
event log;
maintenance log.

The system should degrade gracefully.

If remote communications fail, the node should continue local sensing and logging where safe.

Communications and Logging Requirements

The communications layer must define:

data fields;
logging interval;
alert thresholds;
offline behavior;
time synchronization method;
local retrieval method;
dashboard export format;
data ownership;
privacy considerations where cameras or public-space sensors are used.
Communications and Logging Non-Claims

Remote telemetry is not guaranteed during severe weather unless separately validated.

The system must preserve useful local logs when communications are unreliable.

Layer 6: Operations and Maintenance Layer

The Operations and Maintenance Layer defines how humans keep the system useful.

It includes:

maintenance owner;
inspection schedule;
debris-clearing procedure;
pump inspection;
sensor cleaning;
battery inspection;
enclosure inspection;
log review;
spare-parts list;
escalation procedure;
operator training;
pilot review process.

This layer is mandatory.

A flood-resilience system without maintenance is likely to become abandoned hardware.

Operations and Maintenance Requirements

The maintenance model must identify:

who owns the site;
who can access the site;
who clears debris;
who reviews logs;
who repairs pumps;
who replaces batteries;
who recalibrates sensors;
who approves shutdown;
who receives alerts;
who evaluates pilot outcomes.
Optional Layer 7: Littoral Sentinel Layer

The Littoral Sentinel Layer is a safe water-sensing and ruggedization layer for coastal, estuary, canal, and waterborne conditions.

It may include:

salinity sensing for backflow detection;
tide or water-level correlation;
wave or surge sensing;
hydrophone-style acoustic monitoring for pump cavitation, turbulence, or debris impact;
vibration monitoring;
rugged waterborne sensor housings;
low-power ambient assist for sensors;
confidence-gated classification.

This layer is derived only from safe civilian water-related concepts.

It does not include defense, weapon, targeting, disabling, stealth, or electronic-attack behavior.

Littoral Sentinel Use Cases

Possible use cases include:

detecting seawater backflow;
detecting abnormal canal turbulence;
detecting pump cavitation;
detecting debris strikes;
monitoring coastal surge behavior;
supporting outfall status awareness;
supporting floating solar or buoy health monitoring.
Littoral Sentinel Non-Claims

This layer does not solve floodwater volume.

It improves situational awareness and equipment diagnostics.

Optional Layer 8: Renewable Energy Support Layer

The Renewable Energy Support Layer may include site-specific power additions.

Candidate additions include:

floating solar;
solar canopy;
flexible solar on selected surfaces;
small water-current sensor harvesters;
piezoelectric trickle harvesters for low-power sensors;
osmotic power research module where fresh and salt water meet;
wave-energy sentinel module in coastal zones;
evaporation-driven research module for low-power sensing only.

The primary energy strategy should remain practical: batteries, solar where feasible, grid charging where available, and approved backup energy.

Renewable Energy Support Non-Claims

Small energy harvesters should not be treated as pump power.

Piezoelectric, evaporation, wave-sentinel, and osmotic modules should be treated as research, sensor-support, or niche auxiliary layers unless validated at the site.

Optional Layer 9: Level 2 Building Upgrade Layer

The Level 2 Building Upgrade Layer defines a future path for higher-capacity permanent infrastructure.

A HydroGrid Flood-Resilience Building may include:

intake screening at lower levels;
pump galleries;
debris handling;
protected batteries above flood level;
protected power electronics;
backup energy systems;
water-treatment support;
maintenance shop;
spare-parts storage;
command room;
communications mast;
event logging;
multi-site flood-state classification.

This is not the first recommended deployment.

The building path exists for partners with sufficient funding, engineering capacity, permitting authority, and long-term maintenance capability.

Data Flow

A simplified data flow is:
```
Sensors
  |
  v
Local node controller
  |
  +--> Local event log
  |
  +--> Local status indicator
  |
  +--> Pump/control decision support
  |
  +--> Gateway
          |
          v
      Operator dashboard/export
          |
          v
      Maintenance action / public-works review
```
The system should not depend on continuous cloud access for local safety-relevant logging.

Flood-State Classification

Flood-state classification should be evidence-based.

Candidate states include:

normal;
rainfall active;
water rising;
flood threshold reached;
intake clog suspected;
outlet blockage suspected;
pump active with verified flow;
pump active with poor flow;
pump dry-run suspected;
pump cavitation suspected;
backflow suspected;
salinity increase detected;
sensor fault suspected;
power degraded;
communications degraded;
maintenance required.

The exact state model must be adapted to the pilot site.

Control Philosophy

IX-Bayanihan-HydroGrid should favor operator-support logic over unsafe autonomy.

A proof-of-concept may automatically log and alert.

Pump activation may be automatic only where safe, approved, and reviewed.

Manual override should be available for maintenance and authorized operations.

The system should fail safe where possible.

Safety Philosophy

Safety review is mandatory before field deployment.

Safety topics include:

electrical safety in wet environments;
battery enclosure safety;
public access protection;
trip and entanglement hazards;
pump intake hazards;
discharge hazards;
contaminated water handling;
structural anchoring;
weatherproofing;
lightning exposure;
hydrogen or fuel-cell safety if included;
maintenance crew safety.

The repo does not authorize field installation.

Pilot Architecture

A minimum serious pilot should include:
```
One known flood chokepoint
One valid discharge path
One debris intake assembly
One pump pod or pump cluster
One water-level sensor
One flow meter
One power backup system
One local controller
One local event log
One communications path
One maintenance procedure
One validation plan
One failure-mode review
```
The pilot should be judged by measured results.

Scaling Architecture

The architecture can scale in stages:

Stage 1: Bench Test

Controlled test of sensors, pump flow, power runtime, logging, and basic failure detection.

Stage 2: Controlled Wet Test

Approved non-public wet test using a known water source, known discharge path, and measured flow.

Stage 3: Single HydroGrid Lot Pilot

A bounded field pilot at one selected chokepoint.

Stage 4: Multi-Lot Cluster

Several lots serving related drainage chokepoints or a small basin.

Stage 5: Level 2 Flood-Resilience Building

Permanent higher-capacity infrastructure after evidence justifies expansion.

Acceptance Evidence

Architecture acceptance should be based on measurable evidence.

Evidence may include:

accurate water-level measurement;
verified flow measurement;
successful clog detection;
successful outlet blockage detection;
battery runtime under defined load;
event log completeness;
communications uptime;
maintenance response tracking;
safe shutdown behavior;
operator usability feedback;
post-event review quality.
Architecture Limits

The architecture cannot overcome:

no discharge path;
insufficient receiving capacity;
extreme rainfall beyond system capacity;
major river overflow;
storm surge exceeding local defenses;
unmaintained debris loads;
unsafe electrical installation;
unapproved public-space deployment;
absent maintenance ownership;
unsupported performance claims.
Summary

IX-Bayanihan-HydroGrid is a modular, evidence-first flood-resilience architecture.

It does not try to solve flooding with one device.

It organizes practical flood-support functions into a reviewable system:

move water only where a valid path exists;
measure water before claiming benefit;
treat debris as a primary failure mode;
preserve power for critical functions;
classify failures using multiple signals;
log events for accountability;
require maintenance ownership;
scale only after measured evidence.

The primary system form is the HydroGrid Lot.

The Level 2 building form is a future upgrade path for partners who need higher-capacity permanent infrastructure and have the engineering, permitting, funding, and maintenance capacity to support it.
