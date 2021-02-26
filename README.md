# CORVUS

> Computer Operated and Run Virtually Under Supervision

A robust task automation assistant for managing my personal file system and listening to file system events such as file downloads and pulling certain files into my personal directories. This allows my file system to portable across PCs and other computer systems.

## TODO

- [ ] if (${project}.updatedAt > 30) -> archiveProject(project) && removePotentialNodeModules();
- [ ] if (onFileDownloadDetected().isWhitelistedExtension) -> moveNewFile();

## Abstract

The hope is to have in some sense an automated system deployed to a server, while slave instances exist as event listeners on each owned system. If I download a certain file on one computer, my CORVUS server acts as a dispatcher and does what needs to be done with that file remotely. This could be done locally, but I own many computers. So for example if a project has been updated on one computer, CORVUS will queue a migaration any given computer that isn't currently online. When online, a CORVUS instance will reconnect, and act on that migration. For a git project, it's a simple `git pull`. For more complex scenarios CORVUS will do what needs to be done. If I edit something in my `~/config/` all systems need to be updated for seamless development.
