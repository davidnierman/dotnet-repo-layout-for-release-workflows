# Source Tree Structure 

## Root Directory
 - Git Attributes (`.gitattributes`)
 - Git Ignore (`.gitignore`)
 - Editor Config (`.editorconfig`)
 - Solution File (`*.sln`)
    - Reasons to put in root and not the src
      1. Allows you to edit the three files above^ in Visual Studio
      2. Easier to find where the git and editor configs are
      3. You will know everything in git is relative to this root directory

 ## src Directory
 - all projects will be in some path under the src directory. For Example: `*.csproj` or `*.wixproj` or `*.fsproj`
 - The deployable purpose of the project is what matters when asking the question *"should I create a separate project?"*
 - For this walk-through we will be creating three projects
 1. Server Project 
    - `dotnet new grpc` - stands for Google Remote Procedure Call
 2. Client Project
    - `dotnet new console` - console app
 3. Shared Library (*Potentially*)
    - `dotnet new classlib` - shared functions
 4. Test Library/s (*It is not clear how many test libraries we want until we start coding - because it depends on what code we share*)

 ## Change Log
 - One of the verification process that the PR goes through - "*Does it update the change log appropriately?*"
 - The PR will need to have the feature updates in the PR's description.
