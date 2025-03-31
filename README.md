# Trip-Planner

## Items
- A position has a latitude and a longitude, both numbers. Represented as a 2-element vector containing a latitude
and a longitude
- A road segment has two endpoints, both positions. Represented as a 4-element vector containing the
latitude and longitude of one end position followed by the latitude and
longitude of the other
- A point-of-interest (POI ) has a position, a category (a string), and a name
(a string). The name of a point-of-interest is unique across all points-of-
interest, but a category may be shared by multiple points-of-interest. Each
position can feature zero, one, or more POIs

## Operation

- **locate-all:** 
Takes a point-of-interest category; returns the positions of all points-
of-interest in the given category. The positions can returned be in any
order but the result does not include duplicates.

- **plan-route:** 
Takes a starting position (latitude and longitude) and the name of
a point-of-interest; returns a shortest path from the starting position to
the named point-of-interest. The starting position is at a
road segment endpoint. Returns the empty list if the destination does not
exist or is unreachable.

- **find-nearby:** 
Takes a starting position (latitude and longitude), a point-of-
interest category, and a limit n; returns the (up to) n points-of-interest
in the given category nearest the starting position. You can assume the
starting position is at a road segment endpoint. 

## Input Types

The TripPlanner constructor must take two arguments:
- A vector of raw road segments.
- A vector or raw points-of-interest

## Output Types
- **locate-all:**
must return its result as a linked list (using the cons library) of
raw positions. The elements of the list can be returned in any order, and
each position may only appear once in the result.
- **plan-route:**
must also return a linked list (also using the cons library) of raw
positions. The positions must be in the order in which they appear in the
path from the source to the destination. For non-existent or unreachable
destinations, plan-route must return the empty list.
- **find-nearby:**
must return a linked list (still using the cons library) of raw
points-of-interest. The points-of-interest in the list can be in any order.

## Dependencies
- import cons
- import sbox_hash
- import 'project-lib/dictionaries.rkt'
- import 'project-lib/graph.rkt'
- import 'project-lib/stack-queue.rkt'
- import 'project-lib/binheap.rkt'
