# Optimization: Milk Collection Route Optimization

This project focused on optimizing milk collection routes for 20 farms using a Traveling Salesman Problem-inspired model. The goal was to minimize the total distance traveled while meeting specific constraints related to tanker capacity and milk collection frequency.

## Approach

1. **Data Definition**
    
   - Data was organized into separate lists for farms, coordinates (north and east), milk collection amounts, and collection frequency. The processing facility was designated as farm zero.

3. **Parameter Setup**
   
   - Defined coordinates for all farms and their respective milk requirements.
   - Categorized farms based on collection frequency: "every day" and "every other day."
   - Set the tanker's maximum capacity to 80,000 gallons.

5. **Distance Calculation**
     
   - Calculated Euclidean distances between all farms and the processing facility.
   - Stored distances in a dictionary for use during optimization.

7. **Optimization Model**
    
   - **Decision Variables**:
     
     - Binary variables indicating routes between farms.
     - Continuous variables for milk collected at each farm.

    - **Objective Function**: Minimized total distance traveled.  

    - **Constraints**:
     
     - Tanker capacity: Limited to 80,000 gallons.
     - Frequency constraints: Ensured "every day" farms were visited daily, and "every other day" farms were split over two days.
     - Route constraints: Used the Miller-Tucker-Zemlin (MTZ) formulation to eliminate subtours.


9. **Optimization and Results**  

    - Ran the model to identify optimal routes and schedules.  
   - Example routes and distances:  
     - Route 0 → 9: Distance = 3.16  
     - Route 1 → 0: Distance = 4.24  
     - Route 2 → 4: Distance = 6.32  
     - Route 3 → 2: Distance = 5.00  
     - (And others.)

**Conclusion**

This project provided valuable insights into creating and refining optimization models, particularly in addressing real-world constraints and achieving efficiency in operations.
