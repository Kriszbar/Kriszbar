```mermaid
graph TD
    A[Start] --> B[Decision Node]
    B -->|Yes| C[Process 1]
    B -->|No| D[Process 2]
    C --> E[End of Process 1]
    D --> F{Decision Node 2}
    F -->|Option 1| G[Result 1]
    F -->|Option 2| H[Result 2]

    subgraph SG1 [First Subgraph]
        C --> E
    end

    subgraph SG2 [Second Subgraph]
        F --> G
        F --> H
    end

    %% Styling
    style A fill:#f9f,stroke:#333,stroke-width:4px
    style B fill:#bbf,stroke:#f66,stroke-dasharray: 5, 5
    style SG1 fill:#bbf,stroke:#f66,stroke-width:2px,stroke-dasharray: 5, 5
    style SG2 fill:#fbb,stroke:#f66,stroke-width:2px
