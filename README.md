RAID Calculator

An interactive tool for calculating storage capacities for various RAID configurations.
Functionality

Hard drive selection: Choose between HDD (20-1 TB) and SATA SSD (16-0.48 TB).
Hard drive slots: Up to 12 hard drives can be added.
Hot spares: Configurable number of replacement hard drives.
RAID types: Supports RAID 0, 1, 5, 6, 10, and JBOD.
Calculation: Displays usable storage, parity data, reserved, and unused storage space.
Visualization: Bar charts for storage distribution per RAID type.
Interactivity: Tabs for HDD/SSD, reset function, dropdown for additional RAID types.

File structure

index.html: Main page with HTML, CSS, and JavaScript.
HTML: Structure for tabs, hard drive slots, input fields, and charts.
CSS: Styling for layout, tabs, slots, bar charts, and buttons.
JavaScript: Logic for:
Initialization (init()): Event listener for tabs, buttons, inputs.
Hard drive display (renderSizes(), renderSlots()): Dynamic buttons and slots.
Calculation (computeData()): Storage allocation for RAID types.
Result display (renderResults(), renderChartRow()): Charts and dropdown.
Reset (clearResults()): Deletes results and resets inputs.







Usage

Select HDD or SATA SSD using the tabs.
Click on hard drive sizes to fill slots (max. 12).
Enter the number of hot spares.
Click on "Calculate" for storage allocation.
See the best RAID configurations and select additional types from the dropdown menu.

Technical details

Language: HTML, CSS, JavaScript.
Units: Capacities in TB, binary representation of 1 GB.
RAID calculations:
RAID 0: Full capacity, no protection.
RAID 1: Smallest hard drive as usable capacity.
RAID 5: Capacity minus one hard drive (parity).
RAID 6: Capacity minus two hard drives (parity).
RAID 10: Half of the hard drives × smallest hard drive.
JBOD: Total capacity without redundancy.


Reserved storage: 1% of raw capacity.

Notes

Results are based on a binary representation of 1 GB.
Color coding: Orange (reserved), green (usable), blue (parity), gray (unused).
Responsive design for different screen sizes.
