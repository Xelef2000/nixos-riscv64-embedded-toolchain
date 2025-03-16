# RISCV32 Embedded Toolchain Shell (Nix Flake)

This Nix flake sets up a development shell for the RISC-V embedded toolchain using `pkgsCross.riscv64-embedded` from Nixpkgs. It also creates symlinks to rename `riscv64-none-elf-*` binaries to `riscv64-unknown-elf-*` for compatibility purposes.

## Features
- Provides a ready-to-use RISC-V embedded toolchain.
- Automatically creates symlinks in `/tmp/riscv-toolchain` to map `riscv64-none-elf-*` binaries to `riscv64-unknown-elf-*`.
- Adds the symlinked binaries to the `PATH`.

## Usage

1. Ensure you have Nix installed.
2. Enter the development shell using:
   ```sh
   nix develop
   ```
3. The toolchain will be available, and the `/tmp/riscv-toolchain` directory will contain the symlinked binaries.

## Customization
- Modify `system` in the flake if using a different architecture.
- Change the symlink directory if needed.

## Notes
- The symlinks are created in `/tmp/riscv-toolchain`.
- Ensure `/tmp/riscv-toolchain` is writable when using the shell.

