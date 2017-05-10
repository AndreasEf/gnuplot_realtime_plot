#!/bin/bash
rm /tmp/rand_points.dat
echo -n "Number of points to generate > "
read num_points
echo -n "Time delay(uS) between points > "
read mil_points
echo "generating $num_points points every $mil_points microseconds"
max=num_points
for (( i=1; i <= $max; ++i ))
do
	pointx=$i
	pointy=$(($RANDOM % 1000 | bc))
	echo "$pointx,$pointy" >> /tmp/rand_points.dat
	usleep $mil_points
done
