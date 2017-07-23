IMPLEMENTATION OF DATA STRUCTURES:

The C++ language has many beautiful implementations of data structures that are extremely helpful in solving competitive programming
problems. However there are some of these that result insufficient (std::<set> for Union-Find data structures, for instance).
Others simply arent implemented. For these cases we must create our own libraries wich the functions we will need.

We would like the utilization of our libraries to be as consistent as possible, so as to make the true heart of the problem lie in the
specific fashion in wich we must use an algorithm or data structure in any given circumstance - not the actual implementationof it in code.
For example, in problems that can be solved with a Union-Find data structure, the actual lines of code that make up
our Union-Find library should be very similar!

UNION FIND (1):

class UnionFind{
private:
	vector<int> pset, pweight;
	int numOfSets;
public:
	void init(int n){
		numOfSets = n;
		pset.resize(n); pweight.resize(n); pcolor.resize(n);
		loop(i,n){
			pset[i] = i;
			pweight[i] = 1;
		}
	}
	int findSet(int i){ return (pset[i] == i) ? i : (pset[i] = findSet(pset[i])); }
	void unionSet(int i, int j){
		if(findSet(i) == findSet(j)) return;
		numOfSets--;
		pweight[findSet(i)] += pweight[findSet(j)];
		pweight[findSet(j)] = pweight[findSet(i)];
		pset[findSet(i)] = pset[j];
	}
	bool isSameSet(int i, int j){ return (findSet(i) == findSet(j)); }
	int sizeOfSet(int i){ return pweight[findSet(i)]; }
}

FENWICK TREE / BINARY-INDEXED-TREE:

class FenwickTree{
private: vector<int> ft;
public:
	void init(int n){ ft.resize(n+1) ft.assign(n+1,0) }
	int rsq(int b){
		int ans, k;
		for(; k; b -= )
	}
}
