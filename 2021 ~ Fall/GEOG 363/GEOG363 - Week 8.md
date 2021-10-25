# GEOG363 - Week 8: Vector Analysis II

# Other Vector Layer Tools
- **Clip:**
    - Same principle of intersect
    - "Cookie cutter"; will cut this shape out of a larger area

- **Dissolve:**
    - Merges many polygons into newer aggregate polygons; Ex: dissolving provinces into a larger country
    - "Uses attributes to aggregate unit polygons into lew, larger polygons which contain at least one common attribute from the samller polygons"

- **Merge:**
    - Bringing together 2 adjacent (in space) data layers in order to create a larger database

- **Eliminate:**
    - Used to eliminate polygons with an area less than a certain threshhold value; used to remove slivers
    - Cleans up presentation of polygons and removes statistically insignificant polygons

# Network Analysis
- **Network analysis** = type of spatial vector analysis that requires **topological** data
    - Interested in the relationship between features; Ex: walking distance, metro wait times, traffic patterns, etc.

## Intro to Network Analysis
- A network is a set of interconnected linear features through which materials, goods and people are transporting or along which communication of information is achieved
- System of interconnected lines (edges) and intersections (junctions) that represent possible routes from one location to another
    - Human made networks:
        - Transport:
    - Natural made networks
        - Geometric utility networks

## Network Types
- Transportation/**undirected network**
    - Roads, rails, subways, pedestrian networks that can be travelled in **any directions**

- Geometric utility/**directed network**
    - Water, sewers, natural gas, electrical networks are networks that **only flow in one direction** often due to natural forces

## Example of Applications of Network Analysis
- **Shortest path analysis** = find the shortest parth between two points
- **Service area solver** = find all areas within a set distance that can be reached from one point; determine pizza place service area

## Utility Network
- Utility networks, such as water distribution or electricity network have:
    - A **source**, pushing the resource
    - A **sink**, pulling the resource

- Ex: If a valve fails, how many and which consumers will be affeceted?