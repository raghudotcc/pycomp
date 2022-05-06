# pycomp

Experimental(toy) python compiler written in Python with support for x86 and WASM targets.

## Features

- [x] Implement x86 IR and WAT
- [x] Add closure support
- [x] Primitive Escape Analysis for closure
- [x] Generate Inteference Graph for register allocatoin
- [x] Fixed point register allocation(using graph coloring) for x86
- [x] Create CFG with BB
- [x] Fixed point liveness analysis on the basic blocks
- [x] Basic dead store elimination using liveness analysis
- [x] Constant Propagation/Copy Folding using Local value numbering on the CFG
- [x] Support for Control Flow Statement (Ternary, If and While)
- [x] Support for Lambda Function (Anonymous, Named and Closure)
- [ ] Support for Class
- [x] Support for Comparison and Logical Operator
- [x] Support for Arithmetic Operator
- [ ] Add Single Static Assignment (SSA)
- [ ] Add Dominance Analysis
- [ ] Add Dominance Frontier Analysis
- [ ] Add Reaching Definition Analysis
- [ ] Resolve Phi Nodes
- [x] Convert CRuntime to WASM using Emscripten

## Usage 


1. Compilation:
   
```bash
./pycomp [--wasm | -w] [--x86 | -x] <input_file.py>
```

Flags are optional.
    > `--wasm`: Compile to WebAssembly.
    > `--x86`: Compile to x86-64.
    > `<input_file.py>`: Input file.

### x86

1. Execution:
   
```bash
./input_file_binary
```

### WASM

1. Execution:

Start the web server from the root folder:

```bash
python3 -m http.server
```

2. Checking the output:

- Go to `http://localhost:8000/` on your browser.
- Open the `index.html` file.
- Open DevTools and click on the `Console` tab.
- Call the wasm function that you are interested in. 
  





