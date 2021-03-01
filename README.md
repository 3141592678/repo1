# repo1
#include<iostream>
using namespace std;
template<class key,class other>
class dsT{
public:
    virtual SET<key,other> *find(const key &x)const=0;
    virtual void insert(const SET<key,other>&x)=0;
    virtual ~dsT(){};
};

template<class key,class other>
class bstree:public sdT<key.other>
{;
private:
    struct bnode
    {
    SET<key,other>data;
    bnode *left;
    bnode *right;
    bnode(const SET<key,other>&thedata,bnode *lt=NULL,bnode *rt=NULL):data(thedata),left(lt),right(rt){}
    };
    bnode *root;
public:
    bstree();
    ~bstree();
    SET<key,other>*find(const key &x) const;
    void insert(const<key,other>&x);
private:
     void insert(const SET<key,other>&x,bnode*&t);
    SET<key,other>*find(const key&x,bnode*t) const;
    void makeEmpty(bnode *t);
};

template<class key,class other>
void bstree<key,other>::insert(const SET<key,other>&x)
{
    insert(x,root);
}

template<class key,class other>
void bstree<key,other>::insert(const SET<key,other>&x,bnode*&t)
{
    if(t==NULL)
    {t=new bnode(x,NULL,NULL);
    cout<<-1;}
    else if(x.key<t->data.key)
    {insert(x,t->left);
    cout<<t->data.key;}
    else if(t->data.key<x.key)
    {insert(x,t->right);
    cout<<t->data.key;}
}
