# Misc tips

# Nuget
Get unique sorted list of packages in solution
```powershell
#Execute in Powershell or Visual Studio "Package Manager Console"
Get-Package | select -expand Id | Sort-Object -Unique > D:\packages.txt
```
