# Part 1: Planning and Analysis


## Problem breakdown

The goal of the Booking Rooms problem is to efficently book as few rooms as possible for a conference in order to save money. We are given a premade schedule that cannot be rearanged, complete with start and end times. Our goal is to build an algorithm that finds the maximum number of overlapping talks within the schedule to book the minimum amount of rooms needed.


## Baseline Solution

To create a functional baseline, we followed a simple comparison approach. This code compares each conference block with eachother slowly going down the line and returns which of these conferences overlap with each other.

```text
def Brute(talks):

    Input: List of conferences(talks) of n lengths
    Output: Number of overlapping conferences(talks)

    overlapping = []
    n = len(talks)

    for i in range(n):

        for j in range(i+1,n):

            if talks[i][1] > talks[j][0]:

                overlapping.append(1)

    return overlapping
```























`pseudocode`


You are organizing a conference and are given a list of start and end times for talks. The schedule cannot be changed. As the organizer, you want to reserve as few rooms as possible to save money.


Goal: determine the maximum number of overlapping talks from the schedule so you can book the correct number of conference rooms.


Input: list of tuples of size two, where each tuple corresponds to a scheduled talk and the entries of the tuple correspond to start time and end time of the talk.


Tasks:
Problem Formulation: Break down the project prompt. Clearly define the input parameters, expected outputs, and constraints.
input: talks = [(9, 10), (10, 12), (11, 1), (12, 3)] / number of talks
expected outputs: number of rooms needed minimum in this case 3
constraints: 1 ≤ number of talks or n ≤ 100










Algorithmic Strategy: Select an appropriate design paradigm (e.g., divide-and-conquer, dynamic programming, greedy). Write detailed pseudocode for your proposed solution.
sorting and scanning. What approach we use


talks = [(9, 10), (10, 12), (11, 13), (12, 3)]
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
