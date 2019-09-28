# ICPC-2019-preli

B. The Social Network

Score: 1

CPU: 3s
Memory: 1500MB

Alice wants to build a new social networking site. And you are hired to implement the functionalities of the site.

There are N users in the site. Every user can upload posts in the site and he/she can see his/her posts by default. But if a user wants to see someone else’s post then both of the user must be in the same network. Two users will be in the same network if they are friends or friends’ friends or friends’ friends’ friends and so on. Once two user U and V are in the same network then user U can see all the posts that user V had previously uploaded and going to upload later and vice versa.

You are given Q queries. You need to perform the queries in the given order. Each query can be one of these types.
0 U V, means user U and user V are now friends.
1 U T, means user U uploads a post on the site in time T. Different users can upload posts at the same time. Also a user can upload multiple posts at the same time.
2 U L R, Count the number of posts user U will see from time L to R inclusive. User U will see a post if that post is uploaded between time L to R inclusive and is uploaded by user U or some other user who is in the same network with user U.


Input

The first line contains an integer TC (1 ≤ TC ≤ 4) denoting the number of test cases. Each test case starts with two space separated integers N (1 ≤ N ≤ 105), Q (1 ≤ Q ≤ 3*105) denoting the number of users and number of queries respectively. Next Q lines contains one of these types of queries.

0 U V (1 ≤ U, V ≤ N, U ≠ V)
1 U T (1 ≤ U ≤ N), (1 ≤ T ≤ 109)
2 U L R (1 ≤ U ≤ N), (1 ≤ L ≤ R ≤ 109)


Output

For each test case, print the case number and for each query of type 2 U L R, print the number of posts that user U will see from time L to R inclusive in a new line. You can safely assume that the result of a 2 U L R type query will not be affected by any subsequent queries. Please see sample for details.

Sample
Input	Output
2
3 6
1 2 7
2 1 1 10
0 2 1
2 1 1 10
1 2 1
2 1 1 10
3 7
1 3 2
1 1 100
1 1 2
0 1 3
0 2 1
2 2 1 10
2 1 2 2
