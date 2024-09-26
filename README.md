
# Derivatives Hedging Project

## 1. Overview
This project involves developing a financial valuation and hedging tool for derivative products using **C++**. The tool implements key design and programming principles, alongside the **Black-Scholes** model for pricing derivatives, aiming to provide an efficient solution for valuing and hedging various financial instruments.

## 2. Dependencies and Compilation

### Dependencies:
- **PNL library** 
- **nlohmann-json** 
- **gtest**

### Installation Instructions:

#### 1. Installing the `PNL` library:
```bash
mkdir lib
cd lib
cp /relative/path/to/pnl ./
mkdir build
cd build
cmake ..
chmod +x ../split_linker_command.sh
make
make install
```

#### 2. Installing `nlohmann-json`:
```bash
sudo apt update
sudo apt install nlohmann-json3-dev
```

### Compilation:
1. Create and move to a build directory:
```bash
mkdir build
cd build
```
2. Compile the project:
```bash
cmake -DCMAKE_PREFIX_PATH=relative/path/to/lib/pnl/build/ ..
make
```
3. Run the executable with arguments:
```bash
./yourExecutableName args
```

## 3. VSCode Configuration

To ensure the project compiles properly in **VSCode**:
- Open the `c_cpp_properties.json` file.
- Add the following to the `includePath` section:
```json
"relative/path/to/lib/pnl/build/include/"
```

## 4. Adding an Executable in `CMakeLists.txt`

To add a new executable to the project, modify the `CMakeLists.txt` file:

```cmake
add_executable(yourExecutableName list_of_cpp_files)
target_link_libraries(yourExecutableName
    ${PNL_LIBRARIES}
    nlohmann_json::nlohmann_json
)
```

