# DynamicBoneWizard
A DynamicBone Installer/Configurer Plugin for Neos.

<img src="https://github.com/dfgHiatus/DynamicBoneWizard/blob/main/dynbone.PNG" width="600">

## Usage
1) Go to the releases tab and download the plugin DLL. 
2) Start Neos with the plugin. If everyone else is a different version, you've loaded the Plugin
3) Use a Developer Tool to create an EmptyObject. Attach the component "Add-Ons -> Wizards -> DynamicBoneWizard"
4) Use the UI to setup your avatar

## Disclaimer
As the naming conventions for Dynamic Bone vary greatly, I cannot guarantee this Plugin will detect every proper bone.

Pro Tip: If you start your bone name with <DynBone>, the system will always detect it!

## For Developers and Contributers
If you would like to add the names of dynamic bones to this Plugin, read on!

There are 4 lists of interest the Plugin uses to compare bone names:
- listOfSingletons
-- This is intended for bones that don't typically have symmetry
- listOfPrefixes
- listOfSuffixes
- listOfFullNames

At runtime, the system populates listOfFullNames with :
1) First, the elements of listOfSingletons
2) Then, select an element from listOfPrefixes
3) For every element in listOfSuffixes, append the suffix to the prefix
4) Repeat for all suffixes.
5)  Repeat steps 2-4 until all prefixes have been used

Feel free to add to the list in and IDE, or in game!

## Thank you!
Shoutout to:
- Zyzyl#1441 - I used your MeshCollider Editor as a base lol
- Faolan#0473 - Big brain bird boy
- sls#6766 - RECURSION!!!
