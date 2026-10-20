# Proposed Solution

Assuming NASA uses a hypothetical lunar rover vehicle for space exploration, deriving energy from solar power, the following apparatus can be considered. The lunar rover seeks to integrate antennas to facilitate the ground communication, with certain sensors including:

- Cameras to capture the images of terrain, rocks, and other objects
- LiDAR to provide 3D-mapping and hazard detection through laser imaging
- Vibration sensors to monitor rover health and detect potential obstructions

Effectively, the containerized application deployed in an edge device attached to the rover intends to poll any data captured by the sensors, leveraging the integrated AI model to analyze and process acquired data. Specifically, Java runtime application is deployed via Podman container to process data polled from the sensors. The application applies AI analytics to process data, with the GPU serving as a parallel-processing unit capable of expediting specific AI operative tasks in terrain classification. For instance, Java may read an image from the camera interface, preparing it in the format required for AI analysis. AI results can then be transferred back to Java for organization and potential future use. Podman containerization manages the application container, enabling consistent operation of the runtime environment. The final processed data can be transmitted to the ground operation facility via rover antennae, which can integrate satellite relay to communicate to the facility on earth. Disruption-Tolerant Networking can also apply a means of stable data transmission amidst intermittent communication links in a space environment by storing data in nodes for future relay when communication becomes available.
