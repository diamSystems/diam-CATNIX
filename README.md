## diam CatNix: A Purrfect Playground for Kernel Exploration (Forked from CatK)

**diam Systems** is proud to introduce **diam CatNix**, a lightweight experimental kernel based on the popular **CatK** project. We believe in fostering a playful and educational open-source environment, and diam CatNix embodies that spirit.

**What is diam CatNix?**

diam CatNix is a simple, Unix-like kernel written primarily in C. It serves as a perfect platform for learning kernel development fundamentals and experimenting with innovative functionalities.  Think of it as your own personal kernel sandbox!

**Getting Started with diam CatNix**

**Building Requirements:**

* A Unix-like system or environment (preferably Linux)
* **clang 14+** with support for i686-pc-none-elf (most installations should have this)
* **LLVM lld** (or GNU ld, if configured manually)
* **grub-mkrescue** (usually comes with GRUB) and **xorriso**
* **NASM assembler**
* **GNU make**

**Building diam CatNix:**

With the prerequisites in place, building diam CatNix is straightforward:

1. **Clone the repository:**

   ```bash
   https://github.com/diamSystems/diam-CATNIX.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd diam-CATNIX
   ```

3. **Build (ISO included):**

   ```bash
   make
   ```

   This will create a bootable ISO image in the `out/` folder.

4. **Optional Build Options:**
    * Skip ISO building: `make SKIP_ISO=1`
    * Skip multiboot signature checking: `make SKIP_MB_CHECK=1`
    * Use multiple threads (if applicable): `make -j$(nproc)`

**Running diam CatNix:**

* **Virtualization:** Run diam CatNix using a virtual machine like QEMU or VirtualBox.
* **QEMU with ISO:**

   ```bash
   qemu-system-i386 -cdrom /path/to/diam-catnix.iso
   ```

* **QEMU with Kernel Image:**

   ```bash
   qemu-system-i386 -kernel /path/to/diam-catnix.bin
   ```

   (Kernel image typically located in `out/isodir/boot` or `out/` if not building the ISO)

**Debugging (Optional):**

1. Enable debug symbols: `make clean && DEBUG=1 make`
2. Run QEMU with debugging enabled (refer to "Building it" for details).
3. Use a debugger like GDB or LLDB to step through the code.

**Contributing to diam CatNix**

diam Systems welcomes contributions from all skill levels! If you're passionate about kernel development, we encourage you to:

* Explore the codebase and delve into the world of kernels.
* Propose improvements and share your innovative ideas.
* Collaborate with the community to shape the future of diam CatNix.

**Please refer to the CONTRIBUTING.md file for guidelines on contributing.**

**Get in Touch**

Join the diam Systems community on [insert platform, e.g., Discord server link] to connect with developers, discuss contributions, and be part of the open-source adventure!

**Licensing**

diam CatNix is licensed under the GNU General Public License version 3 (GPLv3). See the LICENSE file for details.
