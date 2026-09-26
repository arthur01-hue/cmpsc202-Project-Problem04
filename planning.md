# Part 1: Planning and Analysis


## Problem breakdown

The goal of the Booking Rooms problem is to efficently book as few rooms as possible for a conference in order to save money. We are given a premade schedule that cannot be rearanged, complete with start and end times. Our goal is to build an algorithm that finds the maximum number of overlapping talks within the schedule to book the minimum amount of rooms needed.


## Baseline Solution

To create a functional baseline, we followed a simple comparison approach. This code compares each conference block with eachother slowly going down the line and returns which of these conferences overlap with each other.

```text
def Brute(talks):

    Input: List of conferences(talks) of n lengths
    Output: Number of overlapping conferences(talks)
    constraints: 1 ≤ number of talks or n ≤ 100

    overlapping = []
    n = len(talks)

    for i in range(n):

        for j in range(i+1,n):

            if talks[i][1] > talks[j][0]:

                overlapping.append(1)

    return overlapping
```

## Purposed Algorithm Strategy

To find the more effective way to book the conferences, we went with a scan-based sorting algorithm. We start it by having it in accending order, then takes the current conference and checks to see if there are others that may overlap with this one, keeping track using the previous most used room with the next. 


def whatever(talks)
    overs=[]
    rooms = 1 (needed because 1 room always)
    max = 1

    for i in range(1, len(talks)):
        before_start, before_end = talks[i -1]
        now_start, now_end = talks[i]


        if now_start < before_end
            overs.append((talks[i-1], talks[i]))
            max = rooms + 1
            return overs
            else
            room = 1

    return rooms, return overs
```