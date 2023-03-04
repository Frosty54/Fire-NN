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
Fire has been thoroughly tested by the CCRL testing group:

3536 Elo on CCRL Blitz
3377 Elo on CCRL 40/15
3589 Elo on CCRL 40/2 FRC
This release (8.3) provides greatly improved play at ultra-fast time controls, eliminating the timeouts experienced by previous versions:

1000ms + 100 ms (avg. game 14 secs)

engine	games	win	loss	draw	timeouts	win%	elo	los
Fire 8.3	1078	+352	-225	=501	0	55.9 %	+42 elo	100%
Fire 8.2	1078	+225	-352	=501	182	45.1%	-42 elo	0%
available Windows binaries
x64 bmi2 = fast pgo binary (for modern 64-bit systems w/ BMI2 instruction set) if you own a Intel Haswell or newer cpu, this compile should be faster.
x64 avx2 = fast pgo binary (for modern 64-bit systems w/ AVX2 instruction set) if you own a modern AMD cpu, this compile should be the fastest.
x64 sse41 = fast pgo binary (for modern 64-bit systems w/ popcnt instruction set)
run 'bench' at command line to determine which binary runs best/fastest on your system. for greater accuracy, run it twice and calculate the average of both results.

please see http://chesslogik.wix.com/fire for more info

compile it yourself
windows (visual studio) use included project files Fire.vcxproj or Fire.sln
minGW run included bash scripts make_sse41.sh, make_bmi2.sh, make_avx2.sh, or make_all.sh

ubuntu type 'make profile-build ARCH=x86-64-bmi2', 'make profile-build ARCH=x86-64-avx2', etc.
uci options
Hash size of the hash table. default is 64 MB.
Threads number of processor threads to use. default is 1, max = 128.
MultiPV number of pv's/principal variations (lines of play) to be output. default is 1.
Contempt higher contempt resists draws.
MoveOverhead Adjust this to compensate for network and GUI latency. This is useful to avoid losses on time.
MinimumTime Absolute minimum time (in ms) to spend on a single move. Also useful to avoid losses on time.
Ponder also think during opponent's time. default is false.
UCI_Chess960 play chess960 (often called FRC or Fischer Random Chess). default is false.
Clear Hash clear the hash table. delete allocated memory and re-initialize.
SyzygyProbeDepth engine begins probing at specified depth. increasing this option makes the engine probe less.
SyzygyProbeLimit number of pieces that have to be on the board in the endgame before the table-bases are probed.
Syzygy50MoveRule set to false, tablebase positions that are drawn by the 50-move rule will count as a win or loss.
SyzygyPath path to the syzygy tablebase files.
acknowledgements
many of the ideas & techiques incorporated into Fire are documented in detail here

Chess Programming Wiki
and some have been adapted from the super strong open-source chess engine

Stockfish
and others

Ippolit
Robbolito
Firebird
Ivanhoe
Houdini
Gull
the endgame table bases are implemented using code adapted from Ronald de Man's

Syzygy EGTBs & probing code
if you are interested in learning about my particular testing methodology, I've explained it in some detail here: http://www.chessdom.com/fire-the-chess-engine-releases-a-new-version/

license
Fire is distributed under the GNU General Public License. Please read LICENSE for more information.

please see http://chesslogik.wix.com/fire for more in
