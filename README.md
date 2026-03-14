import heapq

class PriorityQueue:
    def __init__(self):
        self.queue = []

    def insert(self, item, priority):
        heapq.heappush(self.queue, (priority, item))

    def delete(self):
        if self.is_empty():
            return None
        return heapq.heappop(self.queue)[1]

    def is_empty(self):
        return len(self.queue) == 0

    def peek(self):
        if self.is_empty():
            return None
        return self.queue[0][1]

# Example# Data-structure-pratical-program-28
