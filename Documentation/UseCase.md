### Use cases for WaM-DaM loader and user interface 

**1.	Intended example users to load data to and query it from WaM-DaM**
•	Data managers and administrators at the Division of Water Resources 
•	Water resources engineers at cities, states, and consulting firms 
•	Graduate and undergrad students and professors in the fields of water resources/environmental engineering or similar disciplines 

**2.	Intended example users to query data from WaM-DaM which already has lots of data**
•	All the above users
•	Interested researchers in water management data from any discipline   
•	High school students 


####SWAMPS Model
**How to import the SWAPMS data to WaM-DaM**      
From Omar’s perspective, he has wetland units, attributes, and their data values. He wants to load this data to WaM-DaM. However, WaM-DaM has metadata requirements to load along with the data Omar has. 
There are two steps in building models in WaM-DaM and populating them with data. First, there the user has to build the data templates and then then can 

**Define Data templates** 


1.	Create a new WaM-DaM database file (e.g., OmarModels). This file will contain all the WaM-DaM data for someone which can be backed up or shared altogether. 
2.	Omar has to define his model SWAMPS and give it some descriptions so others can understand what these wetland units mean. This definition is called in WaM-DaM as Data Structure. Part of defining the data structure name, webpage, and description, the user can select a data structure domain (e.g., water supply, wastewater collection, storm water) from a list of pre-defines controlled vocabulary or allows the user to add a new domain (e.g., wetland management) and use it. 
3.	For the SWAMPS data structure (i.e., Model) Omar has to define the types of objects his model has like wetland units, inflow stations, and gates of wetland units. The user can use their own Object Name (i.e., native term) for their model (e.g., wetland_unit). The user can choose to relate (i.e., tag) this native term with a pre-existing controlled term (e.g., Wetland) or they could add a new controlled term if it doesn’t exist. Controlled terms like a Wetland would already belong to categories (e.g., hydro-ecologic). The user also could define a new category if it does not exist. The user could add their own native category of Object Types in their model (i.e., dicked_wetlands).    
4.	Each of these objects has a collection of its own native attributes (e.g., wetland unit area). The user can add attributes to their Object Type. Similar to Object Types, each attribute can be related or tagged to a controlled attribute. The controlled attribute would have controlled categories and the user can add native categories too. Each native attribute must have a unit. The user selects a unit from a pre-existing list or they can add a new one if it doesn’t exist. A unit has a name (e.g., meter) and type (e.g., length) and system (i.e., either US or SI). A software business rule must enforce the consistency units to have the same system for the whole data structure. Probably, the user should choose the system of units, right after they define the data structure. 
In this template step, the user defines a data a model, its objects, and their attributes. This model template is generic and can be applied many times to create multiple data sets for different locations (i.e., networks) as illustrated in the next step.


A.	Populate Data templates manually  
1.	The user chooses one data structure (i.e., model) from a pre-defined list created above to populate it with data for a specific location. This location is called Networks (e.g., Bear River Migratory Bird Refuge). The use defines a network for a specific data structure. A software business rule should enforce this relationship. The network has a vertical datum and a spatial reference that are controlled vocabulary where the user chooses an existing one or they could add a new one. 
2.	The user chooses the defined network above and then they define scenarios that can represent different modeling conditions for their model like “Base Case” and “future”.
3.	The use chooses a scenario in their network and then chooses an object type (i.e., click on it) and create instances of a “node” topology to replicate as many times of them as needed for a specific location (i.e., longitude and latitude) on a preloaded shapefile map. 
4.	For Object types with a “link” topology, the user chooses an Object Type, then they must click on an existing node instance as a start node of the link and then click on a another different existing node instance as an end node. A software business rule must enforce that a link must have a different start and end nodes. Software business rules could also enforce limited kinds of connectivity between links and nodes. For example, a river link object type can connect between a set of defined node object types like reservoirs and head flows. However a river cannot connect between a house as a start point and a sewer connection end node. A user can choose to have as many vertices along the link line. These vertices only help to follow an irregular link through longitudes and latitudes but they have no properties otherwise. 
5.	Each instance should inherit all the attributes and their units of an Object type. A software business rule should inforce this property. In this case, all the instance of the same object type would always have the same set of attributes and units.  
6.	The user can build a network on node and link instances that have no data values for attributes. A dummy attribute called “Object Instances” makes the connection between Instances and Object Attributes at the Mapping Table. This attribute has no unit and cannot have data values. The attribute could have metadata of sources and methods that could explain where this instance came from, how, and by whom.  Sources and methods could be populated and reused for the same data structure and across networks. The user can either select a pre-existing source or method, or they could a new one.  
7.	If the user chooses to populate attributes of instances with data, they must choose a source, method, and the Attribute Type Code (e.g., time series) for their specific instance and its attribute (e.g. inflow). They should also choose if the data values represent input or output of a model. Information about the model could be recorded as a method type and then in the Models metadata table.  The user should be able to apply the same source and method to the same attribute across many instances.  
8.	Once the use chooses the data type for each attribute of each instance, a pop-up fields should open for each data type ready to populate them with data values and their specific metadata. Many of the data values of attribute types like Text Controlled have pre-defined data values as controlled terms. The user should be able to choose a data value from the list of add a new one. An attribute can only have one attribute data type at a time.  The user should be able to apply the same data type to all attributes of instances of the same object type. They also could have different attribute types of the same attribute across instances.  




