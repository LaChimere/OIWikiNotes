# DFS

DFS 伪代码大致如下:

```c++
dfs(v)
{
    visited[v] = true;
    for u in v的相邻结点
        if (!visited[u])
            dfs(u);
}
```

# BFS

BFS 伪代码大致如下:

```c++
bfs()
{
    queue<node> q;
    q.push(s);
    visited[s] = true;
    while (!q.empty())
    {
        auto cur = q.front();
        q.pop();
        for each edge of (s,v)
        {
            if (!visited[v])
            {
                q.push(v);
                visited[v] = true;
            }
        }
    }
}
```

在 BFS 中, 除了使用 `queue`, 还可以使用 `deque` 甚至 `priority_queue`.