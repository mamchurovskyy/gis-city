# Geographic information system

**Geographic information system that interactively implements the functions of analyzing geographic data:**

- Finding the centers of geographic features (buildings);
- Building the shortest route between two buildings;
- Building the shortest route through an arbitrary number of buildings.

---

**What was used?**

- Python 3.10.6;
- PostgreSQL 14;
- [PostGIS](https://postgis.net/) extension for PostgreSQL;
- Jupyter Notebook;
- [ipyleaflet](<https://ipyleaflet.readthedocs.io/en/master/>) for interactive map in Jupyter Notebook.

---

**What was done?**

- Created a new PostgreSQL user and a new database;
- Enabled the `PostGIS` extension for the database;
- Imported shapefiles into the newly created database;
- Created a stored procedure and a table to get and store buildings centers, respectively;
- Created a stored function to build the shortest route between two buildings that are specified by the user as two arbitrary points;
- Created a stored procedure to build the shortest route through an arbitrary number of buildings that are specified by the user;
- Implemented an interactive map with several layers:
  - layer with data on buildings in the city of Poznań;
  - user marker layer;
  - route layer;
- Implemented the calculation of the length of the received route.

---

**Examples**
![Initial view of the interactive map](./screenshots/initial_view.png)
**Figure 1** - Initial view of the interactive map

![Adding markers to an interactive map](./screenshots/markers.png)
**Figure 2** - Adding markers to an interactive map

![Building a route based on user markers](./screenshots/final_route.png)
**Figure 3** - Building a route based on user markers

---

**How to run on your PC**

1. Create new virtual environment, for example:

    ``` bash sh shell zsh
      python -m venv venv
    ```

2. Clone this repository:

    ``` bash sh shell zsh
    git clone https://github.com/mamchurovskyy/gis-city.git
    ```

3. Active virtual environment and install all required libraries using `requirements.txt` file:

    ``` bash sh shell zsh
    pip install -r requirements.txt
    ```

4. Enable notebook extension:

    ``` bash sh shell zsh
    jupyter nbextension enable --py --sys-prefix ipyleaflet
    ```

5. Start Jupyter Notebook:

    ``` bash sh shell zsh
    jupyter notebook
    ```

6. Run all cells and have fun =)
