# FloodSavvy

**FloodSavvy** is a resource that pilots new ways to access and visualize information available from [NOAA’s National Water Model](https://water.noaa.gov/). The web-based interface offers the ability to assess water-related risks, monitor streamflow, and visualize flood inundation extents. It was developed in partnership with six communities across **Vermont** and **Missouri**. In Missouri: City of De Soto, City of Springfield–Greene County, Roaring River State Park. In Vermont: [Mt. Ascutney](https://www.marcvt.org/), [Two Rivers–Ottauquechee](https://www.trorc.org/), and Windham.

## Getting Started

### Clone the repo, checkout this branch
```console
git clone https://github.com/CUAHSI/com_res.git
cd com_res
git checkout develop
```

### Full stack for local development
```console
cp env.template .env
make build-all
make up-all
```
The API will be available at http://0.0.0.0:8000
The UI will be available at http://localhost:5173

To bring the stack down:
```console
make down-all
```
To see logs:
```console
make logs-front
#or
make logs-back
```
## Formatting and linting
```console
# backend:
make format
# frontend:
cd frontend && lint-format-fix
```
Formatting and linting is run with a git pre-commit hook using Husky.
It requires the Docker daemon to be running.
If you are having trouble with the formatting and linting, you can see here how to skip the git hook:
https://typicode.github.io/husky/how-to.html#skipping-git-hooks
However note that this is not recommended -- let's keep our code clean!

## Citation and Acknowledgments

### Cite the Data

The geospatial datasets used by FloodSavvy are documented in the HydroShare collection [FloodSavvy Geospatial Data Collection](https://www.hydroshare.org/resource/1d65ffc2acef4261bffe1be78d24731c/). Cite the collection as:

> Garousi-Nejad, I. (2026). *FloodSavvy Geospatial Data Collection*. HydroShare. https://www.hydroshare.org/resource/1d65ffc2acef4261bffe1be78d24731c/

The collection is shared under the [Creative Commons Attribution 4.0 International license (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Check the license and citation information for each linked dataset before reusing it.

### Development Team and Contributions

FloodSavvy was developed through a collaboration between CUAHSI and the Global Resilience Institute (GRI) at Northeastern University, with support from the Cooperative Institute for Research to Operations in Hydrology (CIROH). The contributions below summarize the team roles published in the project and the work described in the project overview; individual task allocations are not published for every team member.

| Team member | Role | Contribution |
| --- | --- | --- |
| Dr. Anthony Castronova (CUAHSI) | Lead of Research; Co-Principal Investigator | Hydrology expertise and application engineering, including forecast and historical streamflow services and visualization. |
| Devin Cowan (CUAHSI) | Former Research Programmer | Application implementation and maintenance, including frontend and API development. |
| Dr. Irene Garousi-Nejad (CUAHSI) | Research Scientist | Prepared and curated geospatial data; contributed hydrology and flood-modeling expertise; translated user needs into feature requirements and implementation plans. |
| Dr. Kristin Raub (GRI, Northeastern University) | Senior Research Scientist; Principal Investigator | Research leadership and coordination of the community-focused study. |
| Dr. Stephen Flynn (GRI, Northeastern University) | Founding Director; Co-Principal Investigator | Project leadership and research oversight. |
| Dr. Robin White (GRI, Northeastern University) | Distinguished Senior Fellow | Contributed as part of the GRI research team to the collaborative study and resource development. |
| Daniela Rincon Reyes (GRI, Northeastern University) | Senior Research Associate | Contributed as part of the GRI research team to stakeholder-informed resource development. |
| Allison Deese (GRI, Northeastern University) | Pre-Doctoral Fellow | Contributed as part of the GRI research team to stakeholder-informed resource development. |
| Emma Hibbert (GRI, Northeastern University) | Senior Research Associate | Contributed as part of the GRI research team to stakeholder-informed resource development. |
| Nalini Gunawardena (GRI, Northeastern University) | Undergraduate Research Assistant | Contributed as part of the GRI research team to stakeholder-informed resource development. |

The broader research team collaborated with NOAA and community partners in Vermont and Missouri to identify needs, co-design resource capabilities, and iteratively develop FloodSavvy. This work involved the City of De Soto, City of Springfield-Greene County, Roaring River State Park, Mt. Ascutney, Two Rivers-Ottauquechee, and Windham partners. The project was supported by CIROH under NOAA award NA22NWS4320003.