# pcpd

## 1. **Env du Dev:**

-   **Installation du `PNL`:**

```bash
mkdir lib
cd lib
cp /relative/path/to/pnl ./
mkdir build
cd  build
cmake ..
chmod +x ../split_linker_command.sh
make
make install
```

-   **Installation du `nlohmann-json`:**

```bash
sudo apt update
sudo apt install nlohmann-json3-dev.
```

-   **compilation:**

```bash
mkdir build
cd build
cmake -DCMAKE_PREFIX_PATH=relative/path/to/lib/pnl/build/ ..
```

-   **configuration vscode:**

    -   Ouvrir le fichier `c_cpp_properties.json`
    -   Ajouter dans `includePath`: **`"relative/path/to/lib/pnl/build/include/"`**
