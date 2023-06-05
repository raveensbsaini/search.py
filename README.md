# search.py
if you have a sorted list of incrasing order then you can  find a particular number in the list and get back its index. 
def search(list,x,last=None,lo=0):
    if last is None:
        last=len(list)
   
    while lo!=last-1:
        y=(lo+last)//2
        if list[y]>x:
            last=y
        if list[y]<x:
            lo=y
        if list[y]==x:
            return y        
    return None
