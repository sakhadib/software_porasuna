# অ্যাডজাসেন্সি লিস্ট

ধরা যাক আমাদের গ্রাফের এডজাসেন্সি লিস্ট অনেকটা এরকম। আমাদের ৫ টা ভার্টেক্স আছে। 0 থেকে 4. এবারে কোন ভার্টেক্স কোন কোন অন্য ভার্টেক্স এর সাথে যুক্ত সেইটা ঐ ভার্টেক্সের একটা লিস্ট আকারে রেখে দিতে পারি এভাবে,&#x20;

```cpp
0 -> 1 4 
1 -> 0 2 3 4 
2 -> 1 3 
3 -> 1 2 4 
4 -> 0 1 3 
```

তাহলে এইটা আমরা কীভাবে কোড লিখব ? বোঝাই যাচ্ছে আমাদের একটা গ্রাফ ক্লাস বানাতে হবে,

```cpp
class graph{
    public:
    int v; // number of vartex
    vector<int> *adj; //Array of Vector
    graph(int v){
        this->v = v;
        adj = new vector<int>[v]; // array of vector can't be larger than n(V)
    }

    void addEdge(int u, int v){
        adj[u].push_back(v);
        adj[v].push_back(u); //for undirected graph
    }
    
    //To See our graph looks okay or not
    void printGraph(){
        for(int i=0; i<v; i++){
            cout << i << " -> ";
            for(int j=0; j<adj[i].size(); j++){
                cout << adj[i][j] << " ";
            }
            cout << endl;
        }
    }
};
```

এখন মেইন ফাংশনে আমরা আমাদের এজ গুলো ডিকলেয়ার করে দিলেই কেল্লা ফতেহ।

```cpp
int main() {
    graph g(5);
    g.addEdge(0,1);
    g.addEdge(0,4);
    g.addEdge(1,2);
    g.addEdge(1,3);
    g.addEdge(1,4);
    g.addEdge(2,3);
    g.addEdge(3,4);

    g.printGraph();

    return 0;
}
```
