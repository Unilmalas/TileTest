# TileTest
Game of tiles solved with A*

A* pseudo
  push startNode onto openList
  
  while(openList is not empty) {
  
     currentNode = find lowest f=g+h in openList
     if currentNode is final (i.e. current state = goal state), return the successful path
     push currentNode onto closedList and remove from openList
     foreach neighbor (or children-nodes) of currentNode {
		if neighbor in ClosedSet
                continue		// Ignore the neighbour which is already evaluated
         if neighbour/child is not in openList {
                save g, h, and f then save the current parent
                add neighbour/child to openList
         }
         if neighbour/child is in openList but the current g is better than previous g {
                 save g and f, then save the current parent
         }
     }
