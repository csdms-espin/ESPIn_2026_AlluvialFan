
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


