.PHONY: all
.PHONY: clean

FLAGS=-Wall -Wextra -pedantic -O3

all: sse.s sse-palignr.s avx2.s avx512f.s avx512bw.s avx512bw_v2.s

sse.s: sse.cpp
	$(CXX) $(FLAGS) -msse4.1 sse.cpp -S

sse-palignr.s: sse-palignr.cpp
	$(CXX) $(FLAGS) -msse4.1 sse-palignr.cpp -S

avx2.s: avx2.cpp
	$(CXX) $(FLAGS) -mavx2 avx2.cpp -S

avx512f.s: avx512f.cpp
	$(CXX) $(FLAGS) -mavx512f avx512f.cpp -S

avx512bw.s: avx512bw.cpp
	$(CXX) $(FLAGS) -mavx512bw avx512bw.cpp -S

avx512bw_v2.s: avx512bw_v2.cpp
	$(CXX) $(FLAGS) -mavx512bw avx512bw_v2.cpp -S

clean:
	rm *.s
