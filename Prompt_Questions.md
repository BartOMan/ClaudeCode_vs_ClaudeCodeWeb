===

## Prompt #1 

I'm a regular claude code user and a long time claude.ai chat user. 
In Claude Code in Linux, I control my file system & my files get written to my local drive.  I control my installed tools, everything from ripgrep, fd, etc. to the Python environments & packages I make available to Claude.  Locally, Claude has some highly optimized built-in tools like Grep, Glob, etc on my system.   However, Claude controls all server-side tools, such as Webfetch, Websearch, etc.   That's a division that I understand.   

But with the new Claude Code Web and the new Capabilities added to Claude.ai chat, it appears that it's talking about a local component.  It's talking about executing "code", but it doesn't say what code and for what purpose.  And it requires permissions for network exfil, either domain-specific or all domains.  What is leaving my local system & when?   Never mind the security aspects right now.  Suppose I just trust Claude/Anthropic, which I do.  But I still need to understand the mechanics.  Is the local code execution just for building (as it mentions), docs like PDFs, .docx, .pptx, .xlsx files, etc?  What "environment" is it running it?  Is it sandboxed or in a portable docker on my system?    And I see there are downloadable (or maybe just accessable) SKILLs when I can enable and an option to upload my own.  Is that running in the same environment?  Can you give me a bit of background here to help me understand what this is about?   You've actually had the ability to run Javascript for a long time now to test code that you write on your servers.  But it wasn't for building a code base attached to a github repo.

And then there's the Claude Code Web.  I see that they just offered me $1000 credits to try it out.  I'd love to know more-- so I guess I can start reading.  But can you give me a ***comparative overview*** of Claude Code Web vs normal Claude Code (running on Linux).   While I will definitely dig more into docs, it's friday, I'm tired, and I'd love a head start on understanding the full environment of Claude Code Web.   

Here's what I know & understand from using Claude Code, so this is how my thoughts are centered when approaching Claude Code web:   The heart of Claude Code (Linux) is the OS and tools it can access & run, and then the File System, where I can create projects, organize them how I like, store special libraries of file, agents, prompts, download a collection of helpful gits, host local documentation, etc.  The generic file system is central to my understanding.  

So does Claude Code web offer a configured VM/docker/etc running a full Linux OS?
Or is it like Google Colab, running a cloude-based VM, with session-level containerization, running in separate kernels, and configurable, but very ephemeral environments?   If that's the case, then I no longer understand Claude Code on the Web.  

Where is the environment file system managed?  Where are the tools installed?  Where are the Skills, Prompts, special Subagents files stored?  Where is the local component run-- in the cloud, like a Colab or is it running on my local processor?   

Try to run through those defining behaviors/characteristics that Claude Code / Claude Code Web have in common (a table would help).  Then make a table detailing where Claude Code / Claude Code Web differ.  Cover the major areas that define Claude Code, particularly ***TOOLS*** (storage location, runtime environment) on the web version, as well as file system type/location/management.   

Is the file system persistent/expandable/finite?  Or is it ephemeral, pushing the user off to Cloud storage environments such as Github (or even Google / Amazon)?

---

## Prompt #2
The comparison guide you made was outstanding and very helpful.  The PDF was super helpful. 
After reading the document, I now have more questions than ever about workflows.  
It sounds like Github is the basis of persistent file storage, but there is a /workspace location in the container for temporary file storage.   

It sounds like the user has some cleanup to do manually, if they don't want all their files going back to their repo.   What happens if you're in the middle of a code mod and you've broken it?   I guess that's on the user to manage the gh branches.  But the user files, presumably that the user transferred/cloned/mirrored from either a user-local file system to the /workspace (unless you put every single file on your github repo).   How much drive space is available in /workspace?  What are its persistence rules?  If the web session closes, how long before the actual cloud session evaporates into the ether?  (I'm assuming you can re-connect to a session).  If you walk away for lunch, will your session die?  Does it have a cache/backup temporarily for restoring an active session?  

What Ubuntu Linux pre-installed toolsets are available?  What things are at the user's discretion vs completely controlled/managed in by Anthropic?  Are there certain "loadouts", to borrow the FPS game lingo?  If you develop for mobile platforms, what are your options?   What languages are supported (i.e. what toolsets do you have to support them?)   What type of workflows work well in Claude Code Web vs Claude Code?   Where do you normally edit files & setup prompts?  

Can you still instruct Claude to write out summaries, or to help you plan?  Can you save session files?   What is the mechanism for moving files between GH <---> /workspace   or 
between user file system <---> /workspace?   Can you pull files from multiple github repos to reuse common sets of files, prompts, /commands, etc.
Can you quickly download something from the web (extra docs) or transfer files from another repo and tell Claude to read @file.md?   Do you expose a cloud-based drive system so an IDE can work in the /workspace?  Or are you stuck editing files in a web-based app?   

Claude Code environment
Are /commands fully supported?   Are custom /agents fully supported?   Are custom /skill files easily incorporated?  What is available for managing the context window?  Is the prompting fully interactive and can you peek at more detailed thinking?  Can you still control thinking depth with special written commands, like "ultrathink".   What is the maximum size context window available?   Can you include a set of tools/scripts of your own and install them like a package into the environment?    

If you think I've missed some issues, please fill in and then  answer as many questions as you can.  Tables are really nice and preferred.  Please generate a similar type of downloadable report PDF report.  Thanks!

---
