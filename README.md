# greedy--min-meets
{
    public:
    //Function to find the maximum number of meetings that can
    //be performed in a meeting room.
   
    int maxMeetings(int start[], int end[], int n)
    {
        // Your code here
        vector<pair<int,int>>v;
        for(int i=0;i<n;i++)
        {
            v.push_back({end[i],start[i]});
            
        }
        sort(v.begin(),v.end());
        int count=0;
        int max=INT_MIN;
        for(int i=0;i<n;i++){
            if(v[i].second>max)
            {
                max=v[i].first;
                count++;
                
            }
        }
        return count;
    }
};
