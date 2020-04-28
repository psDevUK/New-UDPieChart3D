# New-UDPieChart3D
A new component for UniversalDashboard based on https://github.com/RakanNimer/react-google-charts

## Parameters
Only a few parameter with this component 4 to be more on the ball they are as follows:-
* -Title    this adds a title to the 3D PieChart
* -Height   allows you to set the height string so 400px or 100% is valid
* -Width    allows you to set the width string so 400px or 100% is valid
* -Data     vital that you must construct your data as a 2 dementional array to be passed to the chart with a title

## Example

```
Import-Module -Name UniversalDashboard.Community -RequiredVersion 2.8.1
Import-Module -Name UniversalDashboard.UDPieChart3D
Get-UDDashboard | Stop-UDDashboard
Start-UDDashboard -Port 10005 -Dashboard (
    New-UDDashboard -Title "Powershell UniversalDashboard" -Content {
        $MultiArray = @()
        $MultiArray += , @('Name', 'Age' )
        $MultiArray += , @('Laila-Belle', 11)
        $MultiArray += , @('Pixie', 9)
        $MultiArray += , @('Zelda', 5)
        $MultiArray += , @('Aurora', 3)
        new-udpiechart3d -Id "PIECHART" -Title "New-UDPieChart3D" -data @($MultiArray)
    }
)
```
