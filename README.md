# Mixing OpenStreetMap, Satellite Imagery and Machine Learning

## The problem

OpenStreetMap is an amazing source for geodata. From an empirical point of view at AFD, we've even noticed that in emerging countries, especially in Africa, the accuracy of the platform can beat the competition (Google Maps etc...). More than a map, OSM offers the possibility to query a huge amount of geographical data and point of interest like hospital, university, townhall etc... This data has been useful to build the AFD urban dashboard (data.afd.fr/urban.html).

However, in some specific case, the label used to describe points of interest (POI) can have ambiguous meaning, or not match the ontology used internally at AFD. Therefore there is a need to reclassy those POI. For example, when working with the mobility section, the label "bus station" in OSM ontology was ambiguous and describe at least two different reality: small bus stop and huge bus terminal, and especially in emerging countries context, covered a large range of differents realities: the land used by a bus terminal can be covered or not, buildings can be built around. The label "bus station" is to general to be exploit.

The need to re-label some POI, in order to be more precise, was present.


## The solution

If object is still a non-trivial task in image analysis, even with Machine Learning. But image classification is a more easier task. The biggest advantage of OpenStreetMap is that it gave us the power to know *where* to look. 

The possibility to couple a labeled POI (i.e a point labeled "bus station" in OSM, with coordinates) and satellite imagery make the re-labeling task quite easy with Machine Learning. But there is still a need of a labeled dataset in order to train, test, validate the algorithm. 

In order to labeled data, a web platform has been forked from OpenSolarMap with the possibility for an human to easily label "bus station" and therefore easily create the training dataset. Using web technology allows to do crowdsourcing in the future.

## Limitations

There are too few bus station labeled in African countries so it ws difficult to train an accurate model, and maybe less time consuming to manually relabeled all bus station. But with projects like Accra Mobility, Transport for Cairo, Digital Matatu, the quantity of data on bus station will increase, so it will be useful in the future.

## Technical specifications

** Most of the code has been forked from OpenSolarMap project !**

- Crowdsourcing: Front end using d3, imagery from Mapbox; backend using a PostGis database
- Machine Learning: Transfer Learning with a pre-trained VGG 16 network, with some layers removed.

## How to replicate the project ? 


