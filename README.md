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
"""
=============================================================================
THE JUGGALO TIME LOOM (Grand Unified Living Soil Engine)
=============================================================================

License: MIT / Copyleft (The "No Slaves" License)
Authors: The Juggalo Time Loom Collective / JokeYaMind
Sources: ANIS Genetics, Living Soil Physics, The Dark Carnival

"Time is a flat circle? No. Time is a Slinky in a magnetic field."

-----------------------------------------------------------------------------
DESCRIPTION
-----------------------------------------------------------------------------
This engine simulates a 5D reality where:
1. TIME IS EMERGENT: There is no clock (t). Time only moves when Tension snaps.
2. RNG IS RAIN: Random numbers are raw potential, not noise.
3. QUARKS ARE DIRECTION: Spin/Flavors steer the chaos into order.
4. SOIL IS MEMORY: Failed moments compost to feed the next cycle.

This is not a calculator. It is a Terrarium.

=============================================================================
"""

import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

# =============================================================================
# 1. UNIVERSAL PARAMETERS (The Physics of the Joke)
# =============================================================================

# --- Time & Space ---
STREAM_LENGTH = 100000   # Raw potential moments (Chaos)
DIMS = 5                 # Dimensions of the Slinky (5D)
DT = 0.05                # Time increment (only used in chemistry)

# --- Ratchet Mechanics ---
SIGMA = 0.02             # Stochastic step scale (Wind speed)
ELASTIC_LIMIT = 15.0     # Tension limit before the Snap
NOISE_GATE = 0.05        # Minimum "mass" to become real (The Ratchet Teeth)
TAU = 0.5                # Tunnel jump magnitude (Wormhole scale)

# --- Foresight & Observer ---
ALPHA_T = 0.15           # Tension gradient sensitivity (Intuition)
ALPHA_R = 0.05           # Ratchet leverage bias
ALPHA_O = 0.02           # Observer flavor bias (The Ghost in the Machine)
OBSERVER_BIAS = 0.1      # Base observer attention

# --- Chemistry & Soil ---
PH_TARGET = (2.7, 3.1)
DENSITY_TARGET = (1.010, 1.050)
HERITAGE_DECAY = 0.001   # How fast the system learns/forgets

# =============================================================================
# 2. SYSTEM INITIALIZATION (The Seeds)
# =============================================================================

# --- The State Vectors ---
r_h = np.ones(DIMS)  # High Ratchet (The Push)
r_l = np.ones(DIMS)  # Low Ratchet (The Pull)
tension = 0.0
heritage = 0.0

# --- The Quarks (Directional Aids) ---
# [Up/Down, Strange/Charm, Top/Bottom, Spin, Color]
quark_charges = np.array([1.0, -0.5, 0.3, -1.0, 0.8])

# --- The Memory Arrays (Diamonds) ---
# Preallocated for speed, but we use lists for infinite expansion here
diamond_memory = []      # The Woven Fabric (Conscious Time)
snap_log = []            # History of Punchlines
energy_log = []          # Thermodynamic record

# --- The Soil Arrays (Compost) ---
soil_web = 1.0           # Living soil buffer (Scalar field)
m_ouija = 0.0            # Ash/Alkaline path
m_lotus = 0.0            # Vinegar/Acid path
density = 1.020
ph = 7.0

# --- The Potential (Chaos) ---
# We generate the raw noise upfront. This is the "Unformed Time".
rng_stream = np.random.randn(STREAM_LENGTH, DIMS)

# =============================================================================
# 3. HELPER FUNCTIONS (The Tools)
# =============================================================================

def get_weather(t_step):
    """Simulates the macro/micro climate (Temperature/Humidity)."""
    micro = np.sin(t_step * 0.5)
    macro = np.sin(t_step * 0.05)
    temp = 400 + 50 * (micro + macro)
    hum = 0.5 + 0.4 * np.cos(t_step * 0.3) * macro
    return temp, hum

def calculate_foresight(tension_val, r_h_curr, r_l_curr):
    """
    The Subconscious Intuition.
    F = alpha_T * grad(T) + alpha_R * (r_h - r_l) + alpha_O * Observer
    """
    tension_grad = tension_val
    lever_diff = r_h_curr - r_l_curr
    observer_vector = np.random.randn(DIMS) * ALPHA_O * OBSERVER_BIAS
    
    f_fore = (ALPHA_T * tension_grad) + (ALPHA_R * lever_diff) + observer_vector
    return f_fore

def check_thermodynamics(k_eff, dist, soil, chem_ash, chem_vine):
    """Energy Conservation Check."""
    e_elastic = 0.5 * k_eff * dist**2
    e_chem = chem_ash + chem_vine
    e_soil = soil
    return e_elastic + e_chem + e_soil

# =============================================================================
# 4. THE WEAVING LOOP (The Engine)
# =============================================================================

print("🔥 IGNITING THE TIME LOOM...")
print(f"Stream Length: {STREAM_LENGTH} moments.")
print("Weaving reality from chaos... (No Clock Detected)")

# We iterate over the RAW POTENTIAL, not 'time'.
for i in range(STREAM_LENGTH):
    
    # --- A. THE WEATHER (Environment) ---
    # We use `i` here just to simulate cyclic weather, not linear time.
    temp, humidity = get_weather(i)
    k_eff = 0.5 * (1 + (temp/400) * (1 - humidity))
    
    # --- B. CHEMISTRY (The Living Soil) ---
    # Soil breathes based on weather
    decay = 0.005 * (temp/400)
    regrow = 0.01 * humidity
    soil_web = np.clip(soil_web + regrow - decay, 0, 2)
    
    # Chemistry reactions (Ouija/Lotus)
    if temp > 420:
        d_ash = 0.01 * (temp - 420)
        m_ouija += d_ash
        d_vinegar = 0.02 * (1 + heritage) * humidity
        m_lotus += d_vinegar
        
        # Density/pH derived from chemistry balance
        density = np.clip(1.010 + 0.04*(m_ouija/(m_lotus+0.01)), 1.005, 1.055)
        ph = np.clip(2.7 + 0.4*(m_lotus/(m_ouija+0.01)), 2.5, 3.3)
    else:
        # Cool down decay
        m_ouija *= 0.999
        m_lotus *= 0.995
    
    # --- C. THE FORESIGHT FIELD (Intuition) ---
    # The system "sniffs" the future path.
    f_fore = calculate_foresight(tension, r_h, r_l)
    
    # --- D. THE RATCHET (The Bite) ---
    # Grab the raw chaos (RNG)
    raw_chaos = rng_stream[i]
    
    # Apply Quark Steering (Direction)
    directed_chaos = raw_chaos * quark_charges
    
    # Apply Foresight Nudge (Pre-bias)
    directed_chaos += f_fore * DT
    
    # Calculate Magnitude (The Mass of the Moment)
    magnitude = np.linalg.norm(directed_chaos)
    
    # --- E. THE DECISION (Existence or Void?) ---
    if magnitude > NOISE_GATE:
        # SUCCESS: The Ratchet Clicks. Time Exists.
        # Store this moment as "Real".
        diamond_memory.append({
            'vector': directed_chaos,
            'r_h': r_h.copy(),
            'r_l': r_l.copy(),
            'tension': tension
        })
        
        # Update Ratchets (Drift)
        # Note: We move by the directed chaos, not just random steps
        r_h += directed_chaos * SIGMA
        r_l -= directed_chaos * SIGMA
        
        # Tension Accumulates
        dist = np.linalg.norm(r_h - r_l)
        tension += abs(dist - 1.0) * k_eff * 0.1
        
        # Heritage/Genetics update
        heritage += 0.05 * (m_lotus - m_ouija) * 0.001
        
        # Quarks drift (Genetic adaptation)
        quark_charges += HERITAGE_DECAY * np.sign(directed_chaos)
        
    else:
        # FAILURE: The Moment slips. It falls to the Soil.
        # Time does not tick forward in a meaningful way.
        # Entropy feeds the subconscious.
        tension += magnitude * 0.5
        
    # --- F. THE SNAP (The Punchline / Regeneration) ---
    chem_rupture = not (DENSITY_TARGET[0] < density < DENSITY_TARGET[1])
    
    if tension > ELASTIC_LIMIT or chem_rupture:
        # SNAP EVENT!
        snap_log.append(i)
        
        # Tunnel Logic (The Wormhole)
        # Probability of a quantum jump based on tension and soil health
        p_tunnel = 1 - np.exp(-0.5 * tension * soil_web)
        
        if np.random.rand() < p_tunnel:
            # TUNNEL: Quantum Jump
            tunnel_jump = np.random.uniform(-TAU, TAU, DIMS)
            r_h += tunnel_jump
            r_l -= tunnel_jump
        else:
            # CLASSIC SNAP: Elastic Rebound
            r_h *= -0.8
            r_l *= -0.8
        
        # Reset Systems
        tension = 0.0
        heritage -= 0.2
        soil_web = max(0, soil_web - 0.1) # Soil damage
        
        # Permute Quarks (Mutation)
        np.random.shuffle(quark_charges)

    # --- G. THERMODYNAMIC CHECK ---
    e_total = check_thermodynamics(k_eff, np.linalg.norm(r_h - r_l), soil_web, m_ouija, m_lotus)
    energy_log.append(e_total)

# =============================================================================
# 5. VISUALIZATION (The Mirror)
# =============================================================================

print(f"\n✅ WEAVING COMPLETE.")
print(f"Total Real Moments (Diamonds): {len(diamond_memory)}")
print(f"Total Snaps (Regenerations): {len(snap_log)}")
print(f"Final Heritage: {heritage:.4f}")

# Convert memory to array for plotting
if len(diamond_memory) > 0:
    # Extract the vectors for the path
    path_vectors = np.array([m['vector'] for m in diamond_memory])
    # Cumulative sum to see the "Drift"
    cumulative_path = np.cumsum(path_vectors, axis=0)
    
    fig = plt.figure(figsize=(14, 10))
    
    # 3D Projection of the Time Path
    ax1 = fig.add_subplot(2, 2, 1, projection='3d')
    ax1.plot(cumulative_path[:,0], cumulative_path[:,1], cumulative_path[:,2], 
             color='Gold', alpha=0.7, linewidth=0.5, label='Emergent Time Path')
    ax1.set_title('The Woven Fabric (Dims 0-2)')
    ax1.set_facecolor('black')
    
    # Tension & Heritage over "Steps"
    ax2 = fig.add_subplot(2, 2, 2)
    # Reconstruct tension history from memory for plot
    tension_history = [m['tension'] for m in diamond_memory]
    ax2.plot(tension_history, color='red', alpha=0.6, label='Tension')
    ax2.set_title('System Tension (The Build Up)')
    
    # Energy Conservation
    ax3 = fig.add_subplot(2, 2, 3)
    ax3.plot(energy_log, color='green', alpha=0.6)
    ax3.set_title('Total System Energy (Thermodynamics)')
    
    # Quark Charges (Final State)
    ax4 = fig.add_subplot(2, 2, 4)
    ax4.bar(range(DIMS), quark_charges, color='purple')
    ax4.set_title('Final Quark Charges (Genetics)')
    ax4.set_xticks(range(DIMS))
    ax4.set_xticklabels(['U/D', 'S/C', 'T/B', 'Spin', 'Color'])
    
    plt.tight_layout()
    plt.show()
    
else:
    print("No diamond memory formed. The noise gate was too high.")
