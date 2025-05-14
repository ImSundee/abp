# pooper klipper macro/plugin

add the pooper.cfg to your printer configuration folder. 
use [include ./pooper.cfg] in your printer.cfg to ensure it works.


## For AFC:
in your AFC.cfg

you will want to set the following 

```
# TOOL Cutting Settings
tool_cut: True # Enable Cut macro.
tool_cut_cmd: AFC_CUT           # Cut macro name.

# Park Settings
park: True # Enable Park.
park_cmd: POOPER_PARK

# Poop Settings
poop: True # Enable Poop.
poop_cmd: POOPER

# Kick Settings
kick: False # Enable Kick.
kick_cmd: AFC_KICK              # Kick macro name.

# Wipe Settings
wipe: False # Enable Wipe.
wipe_cmd: AFC_BRUSH             # Wipe macro name.

# Form Tip Settings
form_tip: False # Enable Tip Form.
form_tip_cmd: AFC 
```

Ensure your kick and wipe are set to false as "pooper" will handle it

#Setting up the pooper.cfg

You will want to setup the following for your printer:

variable_brush_start = the left side of your brush
variable_brush_width = 28mm for the a1 mini brush
variable_purge_x = this is the furthest you want it to move to activate the activator giving the pusher full placement, and your nozzle should be roughly in the middle of the pusher box.

I'd recommend homing the printer, leveling ect, then edging to the spots and record the movement. ensure this aligns with the highest Y number your printer can move to as the code will use your y max.

After you will have new macros available to use.

POOPER = poop and brush - returns to last location after
POOPER_PARK = parks the nozzle in the ABP
POOPER_CLEAN = cleans the nozzle

