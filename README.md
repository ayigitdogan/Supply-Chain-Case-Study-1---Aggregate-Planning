# Supply Chain Case Study 1 - Aggregate Planning

In this study, the below supply chain case will be solved using the aggregate planning approach and [PuLP](https://github.com/coin-or/pulp) library.

## Case Definition

Can Caravan is a renowned caravan manufacturer, who offers a variety of 42 models to its
customers. These 42 models are grouped under two main categories with respect to their
manufacturing requirements, i.e. basic and pro series. For the June 2022-May 2023 period,
the company wishes to develop an aggregate production plan.

The monthly demand forecast for different caravan series for the planning period is given
below.

<table>
<thead>
  <tr>
    <th></th>
    <th>Basic</th>
    <th>Pro</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Jun.22</td>
    <td>28</td>
    <td>14</td>
  </tr>
  <tr>
    <td>Jul.22</td>
    <td>20</td>
    <td>10</td>
  </tr>
  <tr>
    <td>Aug.22</td>
    <td>26</td>
    <td>4</td>
  </tr>
  <tr>
    <td>Sep.22</td>
    <td>24</td>
    <td>4</td>
  </tr>
  <tr>
    <td>Oct.22</td>
    <td>18</td>
    <td>6</td>
  </tr>
  <tr>
    <td>Nov.22</td>
    <td>10</td>
    <td>8</td>
  </tr>
  <tr>
    <td>Dec.22</td>
    <td>22</td>
    <td>10</td>
  </tr>
  <tr>
    <td>Jan.23</td>
    <td>20</td>
    <td>12</td>
  </tr>
  <tr>
    <td>Feb.23</td>
    <td>18</td>
    <td>6</td>
  </tr>
  <tr>
    <td>Mar.23</td>
    <td>32</td>
    <td>8</td>
  </tr>
  <tr>
    <td>Apr.23</td>
    <td>34</td>
    <td>14</td>
  </tr>
  <tr>
    <td>May.23</td>
    <td>36</td>
    <td>6</td>
  </tr>
</tbody>
</table>

Cost of producing a basic series caravan is estimated to be $6250, excluding cost of direct
labour. This figure is $9750 for pro series caravans. Considering the direct labour
requirements, a basic series product demands 380 man.hours for production, whereas a pro
series caravan requires 530 man.hours. Holding cost of a basic caravan is estimated to be $250
per caravan per month, whereas it costs $500 to hold one unit of pro caravan in stock for a
month. At the end of May 2022, the company projects to have 8 units of basic model, and 3
units of pro model caravans in it stocks.

Currently the company employs 86 assembly workers, who work 180 hours per month on
average. Average monthly salary of an assembly worker is $420. Workers can be asked to work
overtime, which is limited by 40 hours per month. The hourly fee for overtime is 50% more
than the regular hourly fee.

Considering the administrative costs and inefficiencies during the orientation period, cost of
employing a new worker is estimated to be $800 per worker. During lay-offs, the company
pays $1400 per worker.

## Base Problem 

Formulate and solve the aggregate production planning problem. To
develop the aggregate plan, you will need to construct and solve a linear programming
problem minimizing the overall cost comprised of production, holding inventory and
workforce related (regular time and overtime) costs. Shortages are not allowed.
Draw a bar chart of monthly production and inventory for the board meeting.
Comment on your plan including the total production, inventory, workforce used, and
related costs.

In your solution to the base problem, investigate the inventory projections for both
models. When is it optimal to carry base version in the inventory, and when is it
optimal to carry the pro version in the inventory? When do you keep both models in
the inventory? Explain.

## Extension 1

During the months of December and January you have the option increasing your
regular man-hour capacity by bringing temporary skilled workers from another plant.
Therefore, there is no hiring cost. Including the relocation cost, the total cost of extra
labour force will be $15/hour.

## Extension 2

The gross space requirements of a basic model needs 40 sq meters for storage,
whereas a pro model needs 60 sq meters in the finished goods park of the company.
The company has total parking area of 500 sq meters. Considering this space constraint
would you revise your aggregate plan? The company also has the option of renting
extra parking space for a fee of $1 per sq meter per month. Would you consider making
a rental agreement, and if so for which months?

Production Engineering and Work Study Department warns you that the standard
hours are measured with an error of 10% (i.e., all labor requirement values can change
by 10%). Assuming that the storage constraint is active, how sensitive is your
optimal plan for scenario to changes in the estimation of labor
requirements? Interpret your findings.
