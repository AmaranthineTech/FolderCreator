# ManPage

@Metadata {
    @PageKind(sampleCode)
    @CallToAction(url: "https://github.com/AmaranthineTech/ShellScripts/blob/main/folderCreator.1", purpose: link)
}

Man page file

## folderCreator man page

```md
.\"Copyright (c) 2015-2022 Amaranthine.  All Rights Reserved.
.\"
.\"
.Dd August 10, 2021
.Dt FOLDERCREATOR 1
.Os macOS 11
.Sh NAME
.Nm folderCreator
.Nd Folder creation utility
.\"
.\" ============================================================================
.\" ========================== BEGIN SYNOPSIS SECTION ==========================
.Sh SYNOPSIS
.Nm
.Ar "folder names"
.Op verbs
.\" =========================== END SYNOPSIS SECTION ===========================
.\" ============================================================================
.\"
.\" ============================================================================
.\" ======================== BEGIN DESCRIPTION SECTION =========================
.Sh DESCRIPTION
.Nm
creates 3 folders in the home folder.
In case the folder names are not provided then the command
will create folders with default names "Tools", "Reports", "Help".
.Pp
The user is also prompted via the graphical user interface for names that should be used for the folders.
This is optional and the user can cancel it.
.Pp
There is also the option of getting help via the help verb.
.Pp
- This script is intended for creating the custom folders that are required on all corporate computers.
.Pp
- Run this script on a new computer or a computer being reassigned to another employee.
.Pp
- This script can run on all computers.
.\" ----------------------------------------------------------------------------
.\" ------------------------- BEGIN TERMINOLOGY LIST ---------------------------
.Sh VERBS
.Bl -hang
.It Op Fl h help
Both the options are used to invoke the help documentation.
.It Op Fl v version
Both the options are used to get the version number of the
.Nm
command.
.El
.\" --------------------------- END TERMINOLOGY LIST ---------------------------
.\" ----------------------------------------------------------------------------
.\" ============================================================================
.\" ======================== BEGIN REQUIREMENTS SECTION ========================
.Sh REQUIREMENTS
The following are the minimum requirements to get the script running.
.Bl -hang -offset 4n -width "xxxxxxxxxxxx" -compact
.It Shell:
zsh
.It OS:
macOS Big Sur 11.4 or later
.It Dependencies:
None
.El
.Ev HOME
.\" ============================================================================
.\" ======================== BEGIN INSTALLATION SECTION ========================
.Sh INSTALLATION
.Nm
can be installed anywhere you wish.
However, there are certain locations that are recommended.
.Bl -hang -offset 4n -width "xxxxxxxxxxxx" -compact
.It Location:
/Library/Scripts/
.It Permissions:
rwx r-x r-x
.El
.\" ============================================================================
.\" ======================== BEGIN USAGE SECTION ========================
.Sh USAGE
.Nm
.Ar folder1
.Ar folder2
.Ar folder3
.Pp
Will create folders with your own names.
.Pp
.Nm
.Ar -h
OR
.Nm
.Ar -help
.Pp
Will invoke the help utility.
.Pp
.Nm
.Ar -v
OR
.Nm
.Ar -version
.Pp
Will print the version number in stdout.
.Ss GUI Interaction
In all cases the user is always prompted for entering folder names via the graphical user interface.
Therefore this script triggers a gui popup.
In case this is not the desired behavior then the appropriate lines of code will need to be commented out.
.\" ============================================================================
.\" ======================== BEGIN WARNING/CAUTION SECTION ========================
.Sh WARNING/CAUTION
.Nm
does not perform any validation of names.
The only options that
.Nm
accepts are
.Ar -h
and
.Ar -help
verbs or the
.Ar -v
and
.Ar -version
verbs.
If the script does not see the
.Ar -h
,
.Ar -help
or the
.Ar -v
,
.Ar -version
options then it will assume that the data being passed in is the name of the folder.
The user of the
.Nm
command must ensure that the desired folder names are passed in.
The user will also be prompted, via the graphical user interface, if he/she wishes to provide the names for the folders.
If yes, then there will be subsequent
prompts asking for the folder names.
.\" ============================================================================
.\" ======================== BEGIN EXIT STATUS SECTION =========================
.Sh EXIT STATUS
In most situations,
.Nm
exits 0 on success
.\" ============================================================================
.\" ======================== BEGIN EXAMPLES SECTION ========================
.Sh EXAMPLES
.Nm
.Ar Resources
.Ar Results
.Ar Assistant
.Pp
This will create 3 folders
.Sy Resources
,
.Sy Results
,
.Sy Assistant
,
in the user's home folder.
.Pp
.Nm
.Pp
This will create 3 folders with the default names
.Pp
.Nm
.Ar Apps
.Pp
This will use the
.Sy Apps
name for the first folder but the default names for the last 2 folders.
.\" ============================================================================
.\" ======================== BEGIN DIAGNOSTICS SECTION ========================
.Sh DIAGNOSTICS
The script produces a log file called
.Sy ~/Library/Logs/folderCreator_log_v1-x.log
.Pp
This file is typically located in the user's home folder log folder.
The x represents the version number of
.Nm
.Pp
You can view the logs for each respective version.
.\" ============================================================================
.\" ======================== BEGIN COPYRIGHT SECTION ========================
.Sh COPYRIGHT
Copyright (c) Amaranthine 2015-2021.
All rights reserved.
https://amaranthine.in
.\" ============================================================================
.\" ======================== BEGIN CONTACT SECTION ========================
.Sh CONTACT DETAILS
.An Author: Arun Patwardhan
.Pp
Website: https://amaranthine.in
.Pp
Email: arun@amaranthine.co.in

```

