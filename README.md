# USSR Naval Vessel Inventory Report (COBOL Practice Project)

A batch-processing COBOL program I built to practice sequential file handling, sorting, lookup tables, and report formatting using GnuCOBOL.

## What This Program Does
1. **Reads Input (`UVMF.dat`):** Reads fixed-width 34-character ship records.
2. **Filters & Sorts (`SORTED.dat`):** Keeps only submarines (type `05` or `06`) and major vessels (`tonnage >= 3500`), then sorts them by Location Code and Vessel Type.
3. **Calculates Costs:** Uses 1D and 2D tables (`OCCURS` & `REDEFINES`) to match location/vessel names and calculate monthly operating costs (`Crew × Monthly Rate`).
4. **Generates Report (`USSRSHIP.rpt`):** Prints a clean, grouped inventory report with formatted numbers.

## Files Included
* `USSRSHIP.cbl` – Main COBOL source code (fixed-format, columns 8–72)
* `UVMF.dat` – Sample input data file
* `SORTED.dat` – Sorted intermediate output
* `USSRSHIP.rpt` – Final generated report

## How to Run
Compile and run using GnuCOBOL:
```bash
cobc -x USSRSHIP.cbl
./USSRSHIP
```
