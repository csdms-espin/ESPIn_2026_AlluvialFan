
# ESPIn_2026_AlluvialFan

By: Erica Scarpitti, Zhilin Shi, Shanti Penprase, and Tahmida Sarker Muna

2026 ESPIn short course, Boulder CO. 

Hello! Welcome to our README page. In this notebook, **we create alluvial fans developing off of a mountain ridge.**

To do this, we create a rectangular grid that is elevated and sloped in the upper portion and flat in the bottom portion. 

We then apply the Stream Power And Alluvial Conservation Equation (SPACE) component and the FlowAccumulator component to our grid. 

To simulate erosion from the uplands and deposition to the lowlands using SPACE and FlowAccumulator, we use a for-loop that uses uplift rate as a proxy for the erosion rate to deliver sediment to the lowlands. 

We then plot topographic elevation, soil depth (proxy for sediment movement), and bedrock elevation to see how sediment moves over varying amounts of time. 

Here is a summary of what this code does: 
1. Create a raster grid
2. Add elevation, soil, and bedrock fields
3. Divide the grid into an elevated upland and a low basin
4. Add random roughness to initiate drainage
5. Establish one open outlet boundary
6. Initialize flow routing and the SPACE sediment model
7. Uplift the upland during each timestep
8. Recalculate drainage
9. Erode, transport, and deposit sediment
10. Save each model state as an animation frame
11. Combine the frames into a GIF


The Fire part -
The wildfire section runs after the alluvial fan is built. It uses Landlab’s SPACE model with two custom classes: ErodibilityStepper, which lets fire-boosted sediment erodibility (K_sed) decay back to baseline over time, and Burner, which places random circular fires on the grid and increases K_sed on burned nodes. Each timestep uplifts the mountain, routes water, erodes and transports sediment, applies fire effects, and records sediment flux at the outlet. It can produce several fires per step using a Poisson distribution and tracks cumulative burns on the grid. Fire is represented only as higher sediment erodibility, not changed hydrology, so the main expected result is increased sediment export after burns compared with an unburned fan.

<img width="876" height="612" alt="image" src="https://github.com/user-attachments/assets/ca3997a3-3e2b-4d84-8a2a-8dbd808376b3" />
