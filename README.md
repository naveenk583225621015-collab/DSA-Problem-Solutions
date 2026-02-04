#include <bits/stdc++.h>
using namespace std;

class Solution {
public:
    int getLastMoment(int n, vector<int>& left, vector<int>& right) {
        int last_time = 0;

        // Ants moving to the left
        for (int pos : left) {
            last_time = max(last_time, pos);
        }

        // Ants moving to the right
        for (int pos : right) {
            last_time = max(last_time, n - pos);
        }

        return last_time;
    }
};

// Example Driver Code
int main() {
    Solution ob;

    int n = 4;
    vector<int> left = {2};
    vector<int> right = {0, 1, 3};

    cout << ob.getLastMoment(n, left, right);

    return 0;
}
