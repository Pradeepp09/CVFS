# CVFS
# Customized Virtual File System (VFS)

This project is a simple implementation of a virtual file system (VFS) in C. The VFS provides basic file operations such as create, read, write, open, close, delete, and list files. It also includes file metadata management, such as tracking file sizes, permissions, and inode information.

## Features

- Create regular files with specific permissions
- Read from and write to files
- Open and close files
- Delete files
- List files with their metadata
- Display file information using file names or file descriptors
- Truncate files
- Move file pointers for read/write operations

## Usage

### Commands

The VFS supports the following commands:

- **create**: Used to create a new regular file.
  - `create <FileName> <Permission>`
- **read**: Used to read data from a regular file.
  - `read <FileName> <NumberOfBytes>`
- **write**: Used to write data into a regular file.
  - `write <FileName>`
- **ls**: List all files with their metadata.
- **stat**: Display information of a file using its name.
  - `stat <FileName>`
- **fstat**: Display information of a file using its file descriptor.
  - `fstat <FileDescriptor>`
- **truncate**: Remove data from a file.
  - `truncate <FileName>`
- **open**: Open an existing file.
  - `open <FileName> <Mode>`
- **close**: Close an opened file.
  - `close <FileName>`
- **closeall**: Close all opened files.
- **lseek**: Move the file pointer to a specific location.
  - `lseek <FileName> <Offset> <StartPoint>`
- **rm**: Delete a file.
  - `rm <FileName>`
- **help**: Display help for all commands.
- **exit**: Terminate the VFS.

### Permissions

- `1` : Read Only
- `2` : Write Only
- `3` : Read & Write

### Modes

- `1` : Read Only
- `2` : Write Only
- `3` : Read & Write

## Functions

### Main Functions

- `CreateFile`: Create a new file.
- `rm_file`: Delete a file.
- `ReadFile`: Read data from a file.
- `WriteFile`: Write data to a file.
- `OpenFile`: Open an existing file.
- `CloseByName`: Close a file by its name.
- `CloseAllFile`: Close all opened files.
- `LseekFile`: Move the file pointer to a specific location.
- `ls_file`: List all files with their metadata.
- `fstat_file`: Display file information using a file descriptor.
- `stat_file`: Display file information using a file name.
- `truncate_file`: Remove data from a file.

### Helper Functions

- `man`: Display manual for a specific command.
- `DisplayHelp`: Display help for all commands.
- `GetFDfromName`: Get file descriptor from file name.
- `Get_Inode`: Get inode from file name.
- `CreateDILB`: Create the Disk Inode List Block.
- `InitialiseSuperBlock`: Initialize the superblock.

## Installation and Compilation

1. Clone the repository.
2. Compile the source code using a C compiler. For example:
   ```bash
   gcc VFS.c -o VFS
