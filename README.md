from djitellopy import Tello


tello = Tello()

tello.connect()
tello.takeoff()

#steps 1-3
#takeoff at 60ft
#Fly due east for 50ft at 60ft elevation 
#turn 90 degrees north
tello.move_up(102)
tello.move_forward(183)
tello.rotate_counter_clockwise(90)

#steps 4-5
#fly north 60ft at 60ft elevation
#turn 90 degrees east
tello.move_forward(183)
tello.rotate_clockwise(90)


#steps 6-7
#fly east 30ft at 30ft elevation
#turn 90 degrees south
tello.move_down(90)
tello.move_forward(92)
tello.rotate_clockwise(92)

#steps 8-9
#fly south 30ft at 30ft elevation
#turn 90 degrees east
tello.move_up(32)
tello.move_forward(90)
tello.rotate_clockwise(90)


#steps 10-11
#fly east 60ft at 40ft elevation
#Land 
tello.rotate_counter_clockwise(90)
tello.move_forward(183)

tello.land()
