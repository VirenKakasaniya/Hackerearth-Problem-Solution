 # Copyright (c) VirenKakasaniya. All rights reserved.
 #Problem Statement link--
 #solution is written as below

n=int(input())
arr=list(map(int,input().split()))
nxt=[-1]*n
s=[]
for i in range(n-1,-1,-1):#this loop is used fo find next greater height
    while s!=[] and arr[s[-1]]<arr[i]:
        s.pop()
    if s!=[]:
        nxt[i]=s[-1]
    s.append(i)

ans=0
dp=[0]*n
for i in range(n-1,-1,-1):#this loop is used find xor of heights
    if nxt[i]==-1:
        dp[i]=arr[i]
        ans=max(ans,dp[i])
        continue
    dp[i]=arr[i]^dp[nxt[i]]
    ans=max(ans,dp[i])

print(ans)
