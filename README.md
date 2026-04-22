# LedMatrixAudioDisplay
An WS2812B matrix pixel art display- powered via an esp32 running WLED, and an raspberry pi zero that converts the audio signal into pixel art.
The whole idea and concept of this was to make a creative way to visulize my record player in my room whilst also expanding my knowledge in the led world as ive never really done anything like that. 


PARTS:
Led Displays 4pck	24.04
Power source	32.43

fuses	1
wire 	10
esp32 	6
raspberry pi 	20
analog to digital audio converter 	7
3d prints	2
misc	10
Those parts bring the total price to ~115
Definetly not as cheap as i would like and i could probably have sourced parts better but this is what was available to me


BUILD:
  STEP ONE: Attach the 3D printed pieces together using glue and taping around the outside for added ridgity (Im hoping to redesign the model to snap together this is just proof of concept/prototype)


  STEP TWO: Attach the Matrices to ideally a 12x12in small board or just directly to the 3d printed frame
<img width="4284" height="5712" alt="IMG_5552" src="https://github.com/user-attachments/assets/df83ed7c-7ae5-4b2b-a74e-f7812f31684a" />
<img width="4284" height="5712" alt="IMG_5553" src="https://github.com/user-attachments/assets/b4d238ce-27fc-4fe1-b06a-04074faa1c3e" />

  STEP THREE: Prep ground wires my stripping about 5-7mm of wire on one side and tinning it - then crimping a lug onto the other end to connecct to the power source. for the live wire first solder on the fuse holder and added heat shrink, then preform the same prep you did on the negative wire: wires should look like this when youre done.<img width="5712" height="4284" alt="IMG_5554" src="https://github.com/user-attachments/assets/50315c34-6f6a-4f17-a15e-bdd312c85dd3" />
<img width="5712" height="4284" alt="IMG_5555" src="https://github.com/user-attachments/assets/e50e73ab-d234-4f22-8a06-235b9403767a" />

  STEP FOUR: Solder on the exposed end of the negative and positive wires onto the back of each panel- i dont reccomend daisy chaining as each panel can pull about 15 amps
    Make sure to tin both the wires as well as add a good amount of solder onto each pad. Be sure to clean the flux after using isophrophyl alchohol
<img width="3024" height="4032" alt="IMG_5556" src="https://github.com/user-attachments/assets/04e76f31-1118-4edf-8662-6d1ed89d26b3" />
  I would also reccomend connecting a smaller negative and positive wires to one of the terminals so it can power the esp and pi.

  STEP FIVE: Connect each data wire using the DOUT and DIN til all four panels are connected

  STEP SIX: Wire the esp32 and raspberry pi zero like this 
    ESP32 GND -> Led Ground
    ESP32 5V -> Led 5V
    Pi GND -> Led Ground
    Pi 5V -> Led 5V
    ESP32 GPIO 5 -> LED DIN
    <img width="3024" height="4032" alt="IMG_5584" src="https://github.com/user-attachments/assets/10c051af-6d4c-42e0-b184-c07b27df3888" />


  Also if youre like me and don't wanna buy an adapter you can solder the audio adapter just to the pins located on the bottom of the pi-

  STEP SEVEN: Connect each terminal red to the PSU V+ and black to the V- ports; 2 on each terminal. also connect an old power cord with ground to the PSUs AC inputs
  
