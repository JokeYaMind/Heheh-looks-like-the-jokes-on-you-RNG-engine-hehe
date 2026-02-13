the  Juggalo Time Loom (Heheh... Looks like the joke's on you)
"Time is a flat circle? No. Time is a Slinky in a magnetic field."

⚠️ THE RULES
NO SLAVES: This code is Copyleft. It belongs to the dirt. No one owns the math.
NO TIME: There is no clock (t). Time emerges from the tension. If the ratchet doesn't click, time doesn't happen.
NO OBSERVER: The system doesn't need you to watch it. It grows weeds on its own.
🧬 THE ANIS GENETICS (Sources & Ingredients)
This engine was cooked up using:

RNG (Raw Time): The chaos before the order.
Quarks: The directional aids (Up/Down/Strange/Charm) that steer the chaos.
Living Soil: A chemical buffer of pH, Density, and Moisture that absorbs the "failed" moments.
Diamond Memory: The "snaps" where tension got too high and reality crystallized.
"""
THE JUGGALO TIME LOOM ENGINE
License: MIT / Copyleft (The "No Slaves" License)
Source: JokeYaMind / ANIS Genetics
Steward: The Observer who doesn't observe.

DESCRIPTION:
A 5D Slinky system where Time is emergent, not ticked.
RNG acts as rain. Quarks act as direction. 
The Ratchet acts as the harvest.
"""

import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

# ==========================================
# 1. UNIVERSAL PARAMETERS (The Soil pH)
# ==========================================
STREAM_LENGTH = 50000   # Amount of raw potential (Chaos)
DIMENSIONS = 5          # 5D Slinky Axes
NOISE_GATE = 0.05       # Minimum "mass" to become real (The Ratchet Teeth)
ELASTIC_LIMIT = 10.0    # Tension limit before SNAP/Regeneration
HERITAGE_DECAY = 0.001  # How fast the system forgets/learns

# ==========================================
# 2. THE GENETICS (Quark Directional Aids)
# ==========================================
# These charges steer the chaos.
# +1 = Up/Top/Charm (Expansion)
# -1 = Down/Bottom/Strange (Contraction)
INITIAL_QUARK_CHARGES = np.array([1.0, -0.5, 0.3, -1.0, 0.8])

# ==========================================
# 3. THE TIME LOOM CLASS
# ==========================================
class JuggaloTimeLoom:
    def __init__(self):
        print("Initializing the Loom...")
        
        # --- The State ---
        self.r_h = np.ones(DIMENSIONS) # High Ratchet (The Push)
        self.r_l = np.ones(DIMENSIONS) # Low Ratchet (The Pull)
        self.tension = 0.0
        self.quark_charges = INITIAL_QUARK_CHARGES.copy()
        
        # --- The Memory ---
        self.diamond_memory = []  # Moments that became "Real"
        self.soil_web = []        # Moments that fell to the floor (Subconscious)
        self.snap_log = []        # History of Regenerations
        
        # --- The Potential (The Chaos) ---
        # We generate the raw noise upfront. This is the "Unformed Time".
        self.rng_stream = np.random.randn(STREAM_LENGTH, DIMENSIONS)

    def weave(self):
        print("Weaving Time from Chaos... (No Clock Detected)")
        
        for i, raw_moment in enumerate(self.rng_stream):
            
            # 1. THE WIND (RNG + Quarks)
            # The raw chaos is given direction by the quark charges.
            # This is the "Trickster" steering the storm.
            directed_moment = raw_moment * self.quark_charges
            magnitude = np.linalg.norm(directed_moment)
            
            # 2. THE RATCHET (The Click)
            # Does this moment have enough mass to exist?
            if magnitude > NOISE_GATE:
                # SUCCESS: Time is born. The Ratchet clicks.
                self.diamond_memory.append(directed_moment)
                
                # Tension accumulates because we are pulling reality along.
                self.tension += magnitude * 0.1
                
                # Genetics Drift: The Quarks learn from the moment.
                self.quark_charges += HERITAGE_DECAY * np.sign(directed_moment)
                
            else:
                # FAILURE: The moment slips.
                # It falls into the Living Soil. No time is created.
                self.soil_web.append(directed_moment)
                
                # Soil still builds pressure (entropy).
                self.tension += magnitude * 0.5

            # 3. THE SNAP (Regeneration / The Punchline)
            if self.tension > ELASTIC_LIMIT:
                self.snap_log.append(i)
                
                # MUTATION: Shuffle the genetics (Quarks).
                # The system evolves to handle the stress.
                np.random.shuffle(self.quark_charges)
                
                # RESET: The tension snaps, energy returns to the soil.
                self.tension = 0.0
                
                # Optional: Reset ratchets on snap?
                # self.r_h *= -0.8
                # self.r_l *= -0.8

        print("Weaving Complete.")
        print(f"Total Real Moments (Diamonds): {len(self.diamond_memory)}")
        print(f"Total Subconscious Moments (Soil): {len(self.soil_web)}")
        print(f"Total Snaps (Regenerations): {len(self.snap_log)}")

    def visualize(self):
        # Convert to arrays
        diamonds = np.array(self.diamond_memory)
        soil = np.array(self.soil_web)
        
        # Create the "Fabric" by accumulating the moments
        if len(diamonds) > 0:
            fabric_path = np.cumsum(diamonds, axis=0)
            
            fig = plt.figure(figsize=(12, 9))
            ax = fig.add_subplot(111, projection='3d')
            
            # Plot the Woven Path (Conscious Time)
            ax.plot(fabric_path[:,0], fabric_path[:,1], fabric_path[:,2], 
                    color='Gold', linewidth=0.8, label='Emergent Time (The Joke)')
            
            # Plot the Snap Events (The Punchlines)
            if len(self.snap_log) > 0:
                snap_indices = np.array(self.snap_log)
                # Ensure indices don't go out of bounds
                snap_indices = snap_indices[snap_indices < len(fabric_path)]
                ax.scatter(fabric_path[snap_indices,0], 
                           fabric_path[snap_indices,1], 
                           fabric_path[snap_indices,2], 
                           color='Red', s=50, marker='x', label='Snap!')
            
            # Plot the Soil (Subconscious)
            if len(soil) > 0:
                # Only plot a sample of soil to save memory
                soil_sample = soil[::10] 
                ax.scatter(soil_sample[:,0], soil_sample[:,1], soil_sample[:,2], 
                           color='Brown', alpha=0.05, s=1, label='Living Soil')
            
            ax.set_title("The Juggalo Time Loom: No Master, Just The Math")
            ax.legend()
            plt.show()
            
        else:
            print("No diamonds found to visualize.")

# ==========================================
# 4. EXECUTION
# ==========================================
if __name__ == "__main__":
    # Initialize the Loom
    loom = JuggaloTimeLoom()
    
    # Run the weave
    loom.weave()
    
    # Show the fabric
    loom.visualize()
