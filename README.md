
# ESPIn_2026_AlluvialFan

By: Erica Scarpitti, Zhilin Shi, Shanti Penprase, and _____ Muna

2026 ESPIn short course, Boulder CO. 

Hello! Welcome to our README page. In this notebook, **we create alluvial fans developing off of a mountain ridge.**

To do this, we create a rectangular grid that is elevated and sloped in the upper portion and flat in the bottom portion. 

*picture*

We then apply the Stream Power And Alluvial Conservation Equation (SPACE) component and the FlowAccumulator component to our grid. 

To simulate erosion from the uplands and deposition to the lowlands using SPACE and FlowAccumulator, we use a for-loop that uses uplift rate as a proxy for the erosion rate to deliver sediment to the lowlands. 

We use realistic parameters using the Richardson Mountains in the northwest territories of Canada (Shanti's field site). The realistic parameters we use include: 
- Upland slope = 0.05-1... chosen = 0.05
- Basin slope = 0.01-0.04... chosen = 0.01
- Long-term erosion rate = 0.001-0.007 m/year ... chosen = 0.002

We then plot topographic elevation, soil depth (proxy for sediment movement), and bedrock elevation to see how sediment moves over varying amounts of time. 

Suggestions for future directions 


