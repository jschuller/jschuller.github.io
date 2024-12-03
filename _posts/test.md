graph TD
    A[Obsidian Vault] -->|Text Generator Plugin| B[AI Processing]
    B --> C[Local Models]
    B --> D[Cloud Models]
    A -->|Templater Plugin| E[Jekyll Post Generation]
    E --> F[GitHub Action]
    F -->|Deploy| G[GitHub Pages]
    
    subgraph "AI Models"
    C -->|LM Studio| H[Local WebUI]
    D -->|API| I[Claude via AWS]
    D -->|API| J[Claude Direct]
    end
    
    subgraph "Automation"
    E -->|Front Matter| K[Chirpy Theme]
    F -->|CI/CD| L[Build & Deploy]
    end
    