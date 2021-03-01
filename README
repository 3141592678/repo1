int main(){
 int n,m,s,l,t1,t2,cn=0;
 cin>>n>>m>>s>>l;
 while(m--){
  cin>>t1>>t2;
  v[t1].push_back(t2);
  v[t2].push_back(t1);
 }
 for(vector<int>::iterator it=v[s].begin();it!=v[s].end();it++){
  cn++;
 }
 cout<<cn<<endl;
 return 0;
}
