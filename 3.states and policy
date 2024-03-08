states = [(0, 0), (0, 1), (1, 0), (1, 1)]
actions = {'Up': (-1, 0), 'Down': (1, 0), 'Left': (0, -1), 'Right': (0, 1)}

policy = {
    (0, 0): 'Right',
    (0, 1): 'Down',
    (1, 0): 'Right',
    (1, 1): 'Up'
}

rewards = {
    (0, 0): 0,
    (0, 1): 0,
    (1, 0): 0,
    (1, 1): 1  
}

gamma = 0.9  

def get_next_state(state, action):
    next_state = (state[0] + actions[action][0], state[1] + actions[action][1])
    if next_state in states:
        return next_state
    return state

def get_action(state):
    return policy[state]

current_state = (0, 0)
for _ in range(3):
    action = get_action(current_state)
    next_state = get_next_state(current_state, action)
    reward = rewards[next_state]
    print(f"Current State: {current_state}, Action: {action}, Next State: {next_state}, Reward: {reward}")
    current_state = next_state
