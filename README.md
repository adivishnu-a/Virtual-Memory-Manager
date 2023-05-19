# Virtual Memory Manager

This repository contains a virtual memory manager program implemented in C++. The program simulates a virtual memory system with a translation lookaside buffer (TLB) and a page table. It takes input addresses from a file and translates them to physical addresses using the TLB and page table.

## Features

- Translation Lookaside Buffer (TLB) with a size of 16 entries.
- Page table with a size of 256 entries.
- Physical memory with a size of 65536 bytes.
- Supports reading addresses from a .txt file.
- Simulates values stored at physical addresses using a .bin file
- Calculates TLB hit rate and page table hit rate.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/Virtual-Memory-Manager.git
   ```

2. Compile the `virtualmemorymanager.cpp` file using a C++ compiler:

   ```bash
   g++ virtualmemorymanager.cpp -o virtualmemorymanager
   ```

3. Generate the physical memory file using the `datagen.cpp` file:

   ```bash
   g++ datagen.cpp -o datagen
   ./datagen
   ```

## Usage

1. Create a file named `inputs.txt` and populate it with the virtual addresses you want to translate. Each address should be on a new line.

2. Run the `virtualmemorymanager` executable:

   ```bash
   ./virtualmemorymanager
   ```

3. The program will read the virtual addresses from the `inputs.txt` file, translate them to physical addresses using the TLB and page table, and display the results on the console.

4. The TLB hit rate and page table hit rate will be calculated and printed at the end of the execution.

## File Descriptions

- `virtualmemorymanager.cpp`: Contains the main implementation of the virtual memory manager program. It reads virtual addresses from a file, performs address translation, and displays the results.
- `datagen.cpp`: Generates the physical memory file (`physical_memory.bin`) filled with random data. This file is required for the virtual memory manager program to function properly.

## Contributing

Contributions to this virtual memory manager project are welcome. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
