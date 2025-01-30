<template>
    <div class="p-4 bg-gray-900 text-white font-mono rounded shadow-lg">
      <h1 class="text-xl font-bold mb-4 text-yellow-400">FiveM Handling File</h1>
      <pre class="text-sm">
        &lt;CHandlingDataMgr&gt;
          &lt;HandlingData&gt;
            &lt;Item type="CHandlingData"&gt;
            <!-- Vehicle Basics -->
                <span class="text-yellow-400">--- Vehicle Basics:</span>
                <span class="text-blue-400 clickable" @click="showPopover('handlingName')">handlingName:</span> <span class=text-green-400 > am187</span>
                <span class="text-blue-400 clickable" @click="showPopover('fMass')">fMass:</span><span class="text-green-400"> 2700.0</span>
                <span class="text-blue-400 clickable" @click="showPopover('fInitialDragCoeff')">fInitialDragCoeff:</span><span class="text-green-400"> 5.0</span>
                <span class="text-blue-400 clickable" @click="showPopover('fDownforceModifier')">fDownforceModifier:</span><span class="text-green-400" > 0.0</span>
                <span class="text-blue-400 clickable" @click="showPopover('fPercentSubmerged')">fPercentSubmerged:</span><span class="text-green-400"> 85.0</span>
            <!-- Vehicle Dynamics -->
                <span class="text-yellow-400">--- Vehicle Dynamics:</span>
                <span class="text-blue-400 clickable" @click="showPopover('vecCentreOfMassOffset')">vecCentreOfMassOffset:</span><span class="text-green-400"> x=0.0, y=0.0, z=-0.0</span>
                <span class="text-blue-400 clickable" @click="showPopover('vecInertiaMultiplier')">vecInertiaMultiplier:</span><span class="text-green-400"> x=0.0, y=0.0, z=-0.0</span>
                <span class="text-blue-400 clickable" @click="showPopover('fDriveBiasFront')">fDriveBiasFront:</span><span class="text-green-400" > Fill In</span>
            <!-- Transmission -->
                <span class="text-yellow-400">--- Transmission:</span>
                <span class="text-blue-400 clickable" @click="showPopover('nInitialDriveGears')">nInitialDriveGears:</span><span class="text-green-400" > 1.00</span>
                <span class="text-blue-400 clickable" @click="showPopover('fInitialDriveForce')">fInitialDriveForce:</span><span class="text-green-400"> 1.00</span>
                <span class="text-blue-400 clickable" @click="showPopover('fDriveInertia')">fDriveInertia:</span><span class="text-green-400"> 1.00</span>
                <span class="text-blue-400 clickable" @click="showPopover('fClutchChangeRateScaleUpShift')">fClutchChangeRateScaleUpShift:</span><span class="text-green-400"> 1.00</span>
                <span class="text-blue-400 clickable" @click="showPopover('fClutchChangeRateScaleDownShift')">fClutchChangeRateScaleDownShift:</span><span class="text-green-400"> 1.00</span>
                <span class="text-blue-400 clickable" @click="showPopover('fInitialDriveMaxFlatVel')">fInitialDriveMaxFlatVel:</span><span class="text-green-400"> 200.0</span>
            <!-- Braking and Steering -->
                <span class="text-yellow-400">--- Braking and Steering:</span>
                <span class="text-blue-400 clickable" @click="showPopover('fBrakeForce')">fBrakeForce:</span><span class="text-green-400"> 0.8</span>
                <span class="text-blue-400 clickable" @click="showPopover('fBrakeBiasFront')">fBrakeBiasFront:</span><span class="text-green-400" > 0.8</span>
                <span class="text-blue-400 clickable" @click="showPopover('fHandBrakeForce')">fHandBrakeForce:</span><span class="text-green-400" > 0.8</span>
                <span class="text-blue-400 clickable" @click="showPopover('fSteeringLock')">fSteeringLock:</span><span class="text-green-400"> 40.0 - 45.0</span>
                <span class="text-blue-400 clickable" @click="showPopover('fSuspensionForce')">fSuspensionForce:</span><span class="text-green-400"> 2.5</span>
                <span class="text-blue-400 clickable" @click="showPopover('fTractionLossMult')">fTractionLossMult:</span><span class="text-green-400"> 1.0</span>
            <!-- Tranction Control -->
                <span class="text-yellow-400">--- Tranction Control:</span>
                <span class="text-blue-400 clickable">fTractionCurveMax: </span><span class="text-green-400" @click="showPopover('fTractionCurveMax')">1.0</span>
                <span class="text-blue-400 clickable">fTractionCurveMin: </span><span class="text-green-400" @click="showPopover('fTractionCurveMin')">1.0</span>
                <span class="text-blue-400 clickable">fTractionCurveLateral: </span><span class="text-green-400" @click="showPopover('fTractionCurveLateral')">1.0</span>
                <span class="text-blue-400 clickable">fTractionSpringDeltaMax: </span><span class="text-green-400" @click="showPopover('fTractionSpringDeltaMax')">1.0</span>
                <span class="text-blue-400 clickable">fLowSpeedTractionLossMult: </span><span class="text-green-400" @click="showPopover('fLowSpeedTractionLossMult')">1.0</span>
                <span class="text-blue-400 clickable">fCamberStiffnesss: </span><span class="text-green-400" @click="showPopover('fCamberStiffnesss')">1.0</span>
                <span class="text-blue-400 clickable">fTractionBiasFront: </span><span class="text-green-400" @click="showPopover('fTractionBiasFront')">1.0</span>
                <span class="text-blue-400 clickable">fTractionLossMult: </span><span class="text-green-400" @click="showPopover('fTractionLossMult')">1.0</span>
            <!-- Suspension -->
                <span class="text-yellow-400">--- Suspension:</span>
                <span class="text-blue-400 clickable">fSuspensionForce: </span><span class="text-green-400" @click="showPopover('fSuspensionForce')">1.0</span>
                <span class="text-blue-400 clickable">fSuspensionCompDamp: </span><span class="text-green-400" @click="showPopover('fSuspensionCompDamp')">1.0</span>
                <span class="text-blue-400 clickable">fSuspensionReboundDamp: </span><span class="text-green-400" @click="showPopover('fSuspensionReboundDamp')">1.0</span>
                <span class="text-blue-400 clickable">fSuspensionUpperLimit: </span><span class="text-green-400" @click="showPopover('fSuspensionUpperLimit')">1.0</span>
                <span class="text-blue-400 clickable">fSuspensionLowerLimit: </span><span class="text-green-400" @click="showPopover('fSuspensionLowerLimit')">1.0</span>
                <span class="text-blue-400 clickable">fSuspensionRaise: </span><span class="text-green-400" @click="showPopover('fSuspensionRaise')">1.0</span>
                <span class="text-blue-400 clickable">fSuspensionBiasFront: </span><span class="text-green-400" @click="showPopover('fSuspensionBiasFront')">1.0</span>
            <!-- Anti-Roll Bars -->
                <span class="text-yellow-400">--- Anti-Roll Bars:</span>
                <span class="text-blue-400 clickable">fAntiRollBarForce: </span><span class="text-green-400" @click="showPopover('fAntiRollBarForce')">1.0</span>
                <span class="text-blue-400 clickable">fAntiRollBarBiasFront: </span><span class="text-green-400" @click="showPopover('fAntiRollBarBiasFront')">1.0</span>
                <span class="text-blue-400 clickable">fRollCentreHeightFront: </span><span class="text-green-400" @click="showPopover('fRollCentreHeightFront')">1.0</span>
                <span class="text-blue-400 clickable">fRollCentreHeightRear: </span><span class="text-green-400" @click="showPopover('fRollCentreHeightRear')">1.0</span>
            <!-- Damage -->
                <span class="text-yellow-400">--- Vehicle Damage:</span>
                <span class="text-blue-400 clickable">fCollisionDamageMult: </span><span class="text-green-400" @click="showPopover('fCollisionDamageMult')">1.0</span>
                <span class="text-blue-400 clickable">fWeaponDamageMult: </span><span class="text-green-400" @click="showPopover('fWeaponDamageMult')">1.0</span>
                <span class="text-blue-400 clickable">fDeformationDamageMult: </span><span class="text-green-400" @click="showPopover('fDeformationDamageMult')">1.0</span>
                <span class="text-blue-400 clickable">fEngineDamageMult: </span><span class="text-green-400" @click="showPopover('fEngineDamageMult')">1.0</span>
            <!-- Misc -->
                <span class="text-yellow-400">--- Misc:</span>
                <span class="text-blue-400 clickable">fPetrolTankVolume: </span><span class="text-green-400" @click="showPopover('fPetrolTankVolume')">1.0</span>
                <span class="text-blue-400 clickable">fOilVolume: </span><span class="text-green-400" @click="showPopover('fOilVolume')">1.0</span>
                <span class="text-blue-400 clickable">fSeatOffsetDistX: </span><span class="text-green-400" @click="showPopover('fSeatOffsetDistX')">1.0</span>
                <span class="text-blue-400 clickable">fSeatOffsetDistY: </span><span class="text-green-400" @click="showPopover('fSeatOffsetDistY')">1.0</span>
                <span class="text-blue-400 clickable">fSeatOffsetDistZ: </span><span class="text-green-400" @click="showPopover('fSeatOffsetDistZ')">1.0</span>
                <span class="text-blue-400 clickable">nMonetaryValue: </span><span class="text-green-400" @click="showPopover('nMonetaryValue')">1.0</span>
            <!-- Flags and Handling Flags -->
                <span class="text-yellow-400">--- Flags and Handling:</span>
                <span class="text-blue-400 clickable">strModelFlags: </span><span class="text-green-400" @click="showPopover('strModelFlags')">1.0</span>
                <span class="text-blue-400 clickable">strHandlingFlags: </span><span class="text-green-400" @click="showPopover('strHandlingFlags')">1.0</span>
                <span class="text-blue-400 clickable">strDamageFlags: </span><span class="text-green-400" @click="showPopover('strDamageFlags')">1.0</span>
            <!-- AI Handling -->
                <span class="text-yellow-400">--- AI Handling:</span>
                <span class="text-blue-400 clickable">AIHandling: </span><span class="text-green-400" @click="showPopover('AIHandling')">1.0</span>
            &lt;/Item&gt;
          &lt;/HandlingData&gt;
        &lt;/CHandlingDataMgr&gt;
      </pre>
  
      <!-- Popover -->
      <div v-if="popoverVisible" class="popover bg-white text-black p-4 rounded shadow-lg">
        <button @click="closePopover" class="absolute top-2 right-2 text-red-500 font-bold">&times;</button>
        <h2 class="font-bold mb-2">{{ currentKey }}</h2>
        <p>{{ popoverContent }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        popoverVisible: false,
        currentKey: "",
        popoverContent: "",
        handlingComments: {
            handlingName: "Vehicle spawn code. Used to identify the vehicle in the game.",
            fMass: "Vehicle weight in KG. Affects how heavy the car feels and reacts to collisions.",
            fInitialDragCoeff: "Drag coefficient controls how quickly the car slows down. Value: 10-120 (Higher = quicker slow down, Lower = longer slow down).",
            fDownforceModifier: "Downforce applied to the vehicle. Remove it if the car is sticking to the ground.",
            fPercentSubmerged: "Percentage of the vehicle submerged in water. Affects buoyancy and water handling.",
            vecCentreOfMassOffset: "Center of gravity of the vehicle. Affects stability and roll behavior.",
            vecInertiaMultiplier: "Inertia multiplier. Affects how the vehicle reacts to steering and weight transfer.",	
            fDriveBiasFront : "Front wheel drive bias. Controls how much power is sent to the front wheels.",
            // Transmission
            nInitialDriveGears : "Number of gears in the transmission.",
            fInitialDriveForce : "Initial drive force. Controls how much power is sent to the wheels.",
            fDriveInertia: "Engine responsiveness. Controls how fast the engine revs in gear. Default is 1.0.",
            fClutchChangeRateScaleUpShift : "Clutch change rate scale upshift. Controls how fast the clutch engages during upshifts.",
            fClutchChangeRateScaleDownShift : "Clutch change rate scale downshift. Controls how fast the clutch engages during downshifts.",
            fInitialDriveMaxFlatVel : "Initial drive max flat velocity. Controls the maximum speed the vehicle can reach.",
            // Brakes and Steering
            fBrakeForce : "Brake force. Controls how quickly the vehicle brakes.",
            fBrakeBiasFront : "Front brake bias. Controls how much braking force is applied to the front wheels.",
            fHandBrakeForce : "Handbrake force. Controls how quickly the handbrake stops the vehicle.",
            fSteeringLock : "Steering lock. Controls the maximum angle the wheels can turn.",
            // Tranction Control
            fTractionCurveMax : "Traction curve max. Controls the maximum traction the vehicle can achieve.",
            fTractionCurveMin : "Traction curve min. Controls the minimum traction the vehicle can achieve.",
            fTractionCurveLateral : "Traction curve lateral. Controls the lateral traction of the vehicle.",
            fTractionSpringDeltaMax : "Traction spring delta max. Controls the maximum traction spring delta.",
            fLowSpeedTractionLossMult : "Low speed traction loss multiplier. Controls the traction loss at low speeds.",
            fCamberStiffnesss : "Camber stiffness. Controls the stiffness of the camber.",
            fTractionBiasFront : "Front traction bias. Controls how much traction is applied to the front wheels.",
            fTractionLossMult : "Traction loss multiplier. Controls the traction loss of the vehicle.",
            // Suspension
            fSuspensionForce : "Suspension force. Controls the force applied by the suspension.",
            fSuspensionCompDamp : "Suspension compression damping. Controls the damping of the suspension during compression.",
            fSuspensionReboundDamp : "Suspension rebound damping. Controls the damping of the suspension during rebound.",
            fSuspensionUpperLimit : "Suspension upper limit. Controls the maximum suspension height.",
            fSuspensionLowerLimit : "Suspension lower limit. Controls the minimum suspension height.",
            fSuspensionRaise : "Suspension raise. Controls the suspension raise.",
            fSuspensionBiasFront : "Front suspension bias. Controls the suspension bias towards the front.",
            // Anti-Roll Bars
            fAntiRollBarForce : "Anti-roll bar force. Controls the force applied by the anti-roll bar.",
            fAntiRollBarBiasFront : "Front anti-roll bar bias. Controls the anti-roll bar bias towards the front.",
            fRollCentreHeightFront : "Front roll center height. Controls the height of the front roll center.",
            fRollCentreHeightRear : "Rear roll center height. Controls the height of the rear roll center.",
            // Damage
            fCollisionDamageMult : "Collision damage multiplier. Controls the amount of damage the vehicle takes from collisions.",
            fWeaponDamageMult : "Weapon damage multiplier. Controls the amount of damage the vehicle takes from weapons.",
            fDeformationDamageMult : "Deformation damage multiplier. Controls the amount of deformation the vehicle takes from collisions.",
            fEngineDamageMult : "Engine damage multiplier. Controls the amount of damage the engine takes from collisions.",
            // Misc
            fPetrolTankVolume : "Petrol tank volume. Controls the volume of the petrol tank.",
            fOilVolume : "Oil volume. Controls the volume of the oil tank.",
            fSeatOffsetDistX : "Seat offset distance X. Controls the offset distance of the seat on the X-axis.",
            fSeatOffsetDistY : "Seat offset distance Y. Controls the offset distance of the seat on the Y-axis.",
            fSeatOffsetDistZ : "Seat offset distance Z. Controls the offset distance of the seat on the Z-axis.",
            nMonetaryValue : "Monetary value. Controls the value of the vehicle.",
            // Flags and Handling Flags
            strModelFlags : "Model flags. Controls the flags of the model.",
            strHandlingFlags : "Handling flags. Controls the flags of the handling.",
            // Damage Flags
            strDamageFlags : "Damage flags. Controls the flags of the damage.",
            // AI Handling
            AIHandling : "AI handling. Controls the AI handling of the vehicle.",
        },
      };
    },
    methods: {
      showPopover(key) {
        this.currentKey = key;
        this.popoverContent = this.handlingComments[key] || "No details available.";
        this.popoverVisible = true;
      },
      closePopover() {
        this.popoverVisible = false;
      },
    },
  };
  </script>
  
  <style scoped>
  .clickable {
    cursor: pointer;
    text-decoration: underline;
  }
  
  .popover {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    max-width: 300px;
  }
  </style>
  