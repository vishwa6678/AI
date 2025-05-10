import itertools

def tsp(graph, start):
    vertices = list(graph.keys())
    vertices.remove(start)
    min_path = float('inf')
    best_path = []

    for perm in itertools.permutations(vertices):
        path = [start] + list(perm) + [start]
        cost = sum(graph[path[i]][path[i + 1]] for i in range(len(path) - 1))
        if cost < min_path:
            min_path = cost
            best_path = path

    print("Best path:", ' -> '.join(best_path))
    print("Minimum cost:", min_path)

graph = {
    'A': {'A': 0, 'B': 10, 'C': 15, 'D': 20},
    'B': {'A': 10, 'B': 0, 'C': 35, 'D': 25},
    'C': {'A': 15, 'B': 35, 'C': 0, 'D': 30},
    'D': {'A': 20, 'B': 25, 'C': 30, 'D': 0}
}

tsp(graph, 'A')
