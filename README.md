# Fork of Frosty's Fake Repo
Don't download the release!

c++17
windows & linux
uci
64-bit
smp (to 256 threads)
configurable hash (to 1024 GB)
ponder
multiPV
analysis (infinite) mode
chess960 (Fischer Random)
syzygy tablebases
adjustable contempt setting
fast perft & divide
bench (includes ttd time-to-depth calculation)
timestamped bench, perft/divide, and tuner logs
asychronous cout (acout) class using std::unique_lockstd::mutex
fast alpha-beta search
fire-1052022 is now available

Schachmaschine has undergone months of meticulous analysis and refactoring using many of the most modern C++ tools available today, including Clang, ReSharper C++, and Visual Studio Code Analysis, ensuring the production of extremely fast highly optimized and stable executables.

available windows binaries
x64 avx2 = fast pgo binary (for modern 64-bit systems w/ AVX2 instruction set)
x64 bmi2 = fast pgo binary (for modern 64-bit systems w/ BMI2 instruction set)
x64 sse41 = fast pgo binary (for modern 64-bit systems w/ popcnt instruction set)
strength
SCHACHmaSchinE has been thoroughly tested by the CCRL testing group:

