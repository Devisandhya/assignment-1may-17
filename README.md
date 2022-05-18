# assignment-1may-17
'''lsum=0
        rsum=0
        n=len(arr)
        for i in range(n):
            lsum=0
            rsum=0
            for j in range(i):
                lsum+=arr[j]
            for j in range(i+1,n):
                rsum+=arr[j]
            if lsum==rsum:
                return i
        return -1'''
        n=len(arr)
        pf=[0]*n
        pf[0]=arr[0]
        for i in range(1,n):
            pf[i]=pf[i-1]+arr[i]
        for i in range(n):
            if i==0:
                lsum=0
            else:
                lsum=pf[i-1]
            rsum=pf[n-1]-pf[i]
            if lsum==rsum:
                return i
        return -1
