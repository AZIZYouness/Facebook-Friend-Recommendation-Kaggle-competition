# Facebook-Friend-Recommendation-Kaggle-competition
Given a directed social graph, we have to predict missing links to recommend friends/followers.
### Mapping the problem into supervised learning problem:
We're trying to map this problem to a binary classification task with 0 implying an absence of an edge and 1 implying the presence as y_i's. Now, we need to featurize a pair of vertices (u_i,u_j) such that these features can help us predict the presence/absence of an edge. A simple feature could be number of common-friends to u_i and u_j which is highly indicative of an edge between u_i and u_j. Also we can use the is_he_followed_back feature, page_rank, katz_score, adar_index etc. Then we'll train our ML Models based on these features to predict the presence/absence of an edge.
### Business objectives and constraints:
- Predcting the probability of a link is useful so as to recommend the highest probability links to a user.
- No low-latency requirement.
- We got to suggest connections which are most likely to be correct and we should try and not miss out any connections.
### Data Overview:
Taken data from facebook's recruting challenge on kaggle 
> https://www.kaggle.com/c/FacebookRecruiting
- Data contains two columns: source and destination edge in the directed graph.
- We have 1.86 M nodes and 9.43M edges
