# oso_plantlink
This is a SmartThings DTH for Oso Plantlink soil moisture sensors.  It is based on the Plantlink 2015 OsoTech DTH. 

I added Capability "battery" and Capability "water", so that I could better monitor the devices using SmartTiles and CoRE.  

"Battery" attribute just mirrors the existing linkBatteryLevel attribute.  

"Water" attribute is based on the existing plantStatus attribute.  According to SmartThings' capability reference (http://docs.smartthings.com/en/latest/capabilities-reference.html#water-sensor), "water" sensors can only be  "dry" or "wet", so the "water" attribute will:

* read "dry" if plantStatus is "dry", "needs water", or "too dry" and water sensor capabilities, or
* read "wet" if plantStatus is "good", "too wet", or "watered"
 

