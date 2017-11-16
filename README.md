# Mixing OpenStreetMap, Satellite Imagery and Machine Learning

## The problem

OpenStreetMap is an amazing source for geodata. From an empirical point of view at AFD, we've even noticed that in emerging countries, especially in Africa, the accuracy of the platform can beat the competition (Google Maps etc...). More than a map, OSM offers the possibility to query a huge amount of geographical data and point of interest like hospital, university, townhall etc... This data has been useful to build the AFD urban dashboard (data.afd.fr/urban.html).

However, in some specific case, the label used to describe points of interest (POI) can have ambiguous meaning, or not match the ontology used internally at AFD. Therefore there is a need to reclassy those POI. For example, when working with the mobility section, the label "bus station" in OSM ontology was ambiguous and describe at least two different reality: small bus stop and huge bus terminal, and especially in emerging countries context, covered a large range of differents realities: the land used by a bus terminal can be covered or not, buildings can be built around. The label "bus station" is to general to be exploit.

The need to re-label some POI, in order to be more precise, was present.


## The solution

If object is still a non-trivial task in image analysis, even with Machine Learning. But image classification is a more easier task. The biggest advantage of OpenStreetMap is that it gave us the power to know *where* to look. The possibility 

## Technical specifications

## How to replicate the project ? 
