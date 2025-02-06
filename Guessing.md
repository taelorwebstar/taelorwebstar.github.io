```mermaid
flowchart TD
    A[Start Game] --> B[Generate Random Number]
    B --> C[Ask Player to Guess Number]
    C --> D[Player Guess Input]
    D --> E{Is Guess Correct?}
    
    E -- Yes --> F[Player Wins!]
    F --> G{Play Again?}
    
    G -- Yes --> B[Generate Random Number]
    G -- No --> H[End Game]
    
    E -- No --> I{Is Guess Too High?}
    
    I -- Yes --> J[Hint: Too High!]
    J --> C[Ask Player to Guess Again]
    
    I -- No --> K[Hint: Too Low!]
    K --> C[Ask Player to Guess Again]
    
    H --> I[Exit]
