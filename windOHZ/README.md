# winDohs

SandBox Configuration

## Kata Zero

```bash
dotnet tool install --global wix
dotnet tool update --global wix
dotnet tool list --global
dotnet nuget add source https://github.com/wixtoolset/index.json --name wixtoolset
dotnet nuget list source
dotnet nuget remove source wixtoolset
```


## Kata One

```bash
new-guid
```

```ep2.wxs
<Wix xmlns="http://wixtoolset.org/schemas/v4/wxs">
  <Package 
      Manufacturer="Deployment Dojo"
      Name="~Ep2"
      Version="0.9"
      UpgradeCode="28a59869-cc55-47da-8a46-abbd556d3a1b">
  
    <StandardDirectory Id="ProgramFilesFolder">
      <Directory Name="~Ep2">
        <Component Id="c1">
          <File Source="ep2.txt" />
        </Component>
      </Directory>
    </StandardDirectory>

    <Feature Id="Main">
      <ComponentRef Id="c1" />
    </Feature>
    
  </Package>
</Wix>
```

## Kata Two

```bash
clear
git status
ls
rm .\dojo.msi, .\dojo.wixpdb, cab1.cab
wix build .\package.wxs -o dojo.msi
start dojo.wsb
```

C:\Users\Default\AppData\Roaming