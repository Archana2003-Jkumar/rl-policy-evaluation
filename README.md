# POLICY EVALUATION
## AIM
To code a python program to evaluate two policies and find which is the best policy.
## PROBLEM STATEMENT
Slippery walk five MDP.
## POLICY EVALUATION FUNCTION
### Policy 1:
```
def policy_evaluation(pi, P, gamma=1.0, theta=1e-10):
    prev_V = np.zeros(len(P), dtype=np.float64)
    # Write your code here to evaluate the given policy
    while True:
      V = np.zeros(len(P))
      for s in range (len(P)):
        for prob, next_state,reward,done in P[s] [pi (s)]:
          V[s] += prob*(reward + gamma * prev_V[next_state] *(not done))
      if np.max(np.abs(prev_V - V))<theta:
        break
      prev_V = V.copy()
    return V

# Code to evaluate the first policy
V1 = policy_evaluation(pi_1, P)
print_state_value_function(V1, P, n_cols=7, prec=5)
```
### Policy 2:
```
def policy_evaluation(pi, P, gamma=1.0, theta=1e-10):
    prev_V = np.zeros(len(P), dtype=np.float64)
    # Write your code here to evaluate the given policy
    while True:
      V = np.zeros(len(P))
      for s in range (len(P)):
        for prob, next_state,reward,done in P[s] [pi (s)]:
          V[s] += prob*(reward + gamma * prev_V[next_state] *(not done))
      if np.max(np.abs(prev_V - V))<theta:
        break
      prev_V = V.copy()
    return V

V2 = policy_evaluation(pi_2, P)
print_state_value_function(V2, P, n_cols=7, prec=5)
```
## OUTPUT:
### Policy1 :
![image](https://github.com/Archana2003-Jkumar/rl-policy-evaluation/assets/93427594/b384f4ab-b0de-4ec8-acd3-9bd24c8721ec)
### Policy2 :
![image](https://github.com/Archana2003-Jkumar/rl-policy-evaluation/assets/93427594/d1bb1ac4-ad41-4af1-8ed2-90feceddaaed)
## State value function:
### Policy 1:
![image](https://github.com/Archana2003-Jkumar/rl-policy-evaluation/assets/93427594/981c9866-d9da-4574-834c-d182a42af2be)
### Policy 2:
![image](https://github.com/Archana2003-Jkumar/rl-policy-evaluation/assets/93427594/1cc3fcc9-4378-4e83-b083-a7cbf5d73b96)
![image](https://github.com/Archana2003-Jkumar/rl-policy-evaluation/assets/93427594/73f93f4e-89bb-44e5-bba4-919697fec646)
## RESULT:
Hence the best policy has been evaluated successfully.
