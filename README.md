# Trip-Planner


### Operation
locate-all Takes a point-of-interest category; returns the positions of all points-
of-interest in the given category. The positions can returned be in any
order you want, but the result should not include duplicates.
plan-route Takes a starting position (latitude and longitude) and the name of
a point-of-interest; returns a shortest path from the starting position to
the named point-of-interest. You can assume the starting position is at a
road segment endpoint. Returns the empty list if the destination does not
exist or is unreachable.
find-nearby Takes a starting position (latitude and longitude), a point-of-
interest category, and a limit n; returns the (up to) n points-of-interest
in the given category nearest the starting position. You can assume the
starting position is at a road segment endpoint. Resolve ties however you
want, and order points-of-interest within the list in any order you want.
