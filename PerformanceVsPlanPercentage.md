PerformanceVsPlanPercentage = 
DIVIDE(
    [ActualPerformance] - [PlannedPerformance],
    [PlannedPerformance],
    0
) * 100
/*
In this measure:
[ActualPerformance] should be replaced with your actual performance measure or column.
[PlannedPerformance] should be replaced with your planned performance measure or column.
DIVIDE function is used to safely perform division. The third parameter (0) is the optional parameter for handling division by zero. If the [PlannedPerformance] is zero, the result of the division will be 0.
The result is multiplied by 100 to convert it into a percentage.
Make sure that both [ActualPerformance] and [PlannedPerformance] are either measures or aggregated columns to ensure correct calculations, especially when dealing with filters or slicers in your reports.
*/
