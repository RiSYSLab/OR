# Colored Traveling Salesman Problem Dataset

This dataset contains benchmark instances for Colored Traveling Salesman Problems (CTSP) and related CBTSP instances. The files are stored in a TSPLIB-style plain-text format.

## Directory Structure

```text
CBTSP-Eil/
CBTSP-Fnl/
CBTSP-Gr/
CTSP200-4/
CTSP400-6/
CTSP600-4/
CTSP800-6/
CTSP1000-5/
CTSP1200-6/
CTSP1400-8/
CTSP1600-10/
```

## Instance Naming

- `CTSP<number_of_nodes>-<number_of_salesmen>`  
  Example: `CTSP400-6` means 400 nodes and 6 salesmen/color sets.
- `CBTSP-Eil`, `CBTSP-Fnl`, `CBTSP-Gr`: CBTSP instance families.

## File Format

Each instance file mainly contains the following fields:

```text
NAME : instance name
COMMENT : description
TYPE : problem type, e.g., CBnTSP
DIMENSION : number of nodes
SALESMEN : number of salesmen
EDGE_WEIGHT_TYPE : distance type, e.g., EUC_2D
NODE_COORD_SECTION : node coordinates
CTSP_SET_SECTION : node sets for each salesman/color
DEPOT_SECTION : depot/start node
EOF : end of file
```

## Example

```text
NAME : eil21-2
COMMENT : 21-city problem (Christofides/Eilon)
TYPE : CBnTSP
DIMENSION : 21
SALESMEN : 2
EDGE_WEIGHT_TYPE : EUC_2D
NODE_COORD_SECTION
1 42 41
2 32 22
3 30 40
...
21 38 35
CTSP_SET_SECTION
1 2 3 4 5 6 -1
2 7 8 9 10 11 -1
DEPOT_SECTION
1
-1
EOF
```

## Notes

- `EDGE_WEIGHT_TYPE: EUC_2D` means two-dimensional Euclidean distance.
- In `CTSP_SET_SECTION`, the first integer in each line is the salesman/color ID. The following integers are nodes assigned to that set. `-1` terminates the line.
- `DEPOT_SECTION` defines the depot/start node. `-1` terminates the section.
- Some instances are derived from TSPLIB or CTSP-related literature.