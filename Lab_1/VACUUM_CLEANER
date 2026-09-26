class VacuumCleaner:
    def __init__(self):
        self.position = [0, 0]
        self.direction = "RIGHT"

    def move_forward(self):
        if self.direction == "RIGHT":
            self.position[1] += 1
        elif self.direction == "LEFT":
            self.position[1] -= 1
        elif self.direction == "UP":
            self.position[0] -= 1
        elif self.direction == "DOWN":
            self.position[0] += 1

        print("Moving", self.direction, "->", self.position)

    def turn_left(self):
        directions = ["UP", "LEFT", "DOWN", "RIGHT"]
        self.direction = directions[
            (directions.index(self.direction) + 1) % 4
        ]
        print("Turned LEFT ->", self.direction)

    def turn_right(self):
        directions = ["UP", "RIGHT", "DOWN", "LEFT"]
        self.direction = directions[
            (directions.index(self.direction) + 1) % 4
        ]
        print("Turned RIGHT ->", self.direction)

    def obstacle_found(self):
        print("Obstacle found!")
        self.turn_right()

    def wall_found(self):
        print("Wall found!")
        self.turn_left()


# Create vacuum
vacuum = VacuumCleaner()

# Example movements
vacuum.move_forward()
vacuum.move_forward()

# Obstacle detected
vacuum.obstacle_found()

vacuum.move_forward()
vacuum.move_forward()

# Wall detected
vacuum.wall_found()

vacuum.move_forward()
