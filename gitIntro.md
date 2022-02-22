# Introduction to Git

## Version Control

    version control systems allow you to revisit previous versions of a file by recording changes, allowing you to revert files, track modifications, and compare changes.

    Local Version Control
        - a database on your hard disk that stores file changes
    
    Centralized Version control
        - entails a single server storing all changes and file versions, accesible by multiple people
    
    Distributed Version Control
        - allows the creation of mirrored repos (backups) in case of failure of the CVCS server
    
    What is Git?
        - snapshots
            - git is a DVCS that stores data as snapshots and creates references to their location
        - local operations
            - necessary info can be found locally, allowing for faster workflow without needing to fetch from the server and the ability to work offline
        - tracking changes
            - every change applied it tracked by Git, and it detects corruption or data loss
        - loss of data
            - minimizes possibility of irreversible damage by making it difficult to lose snapshots
        - states
            - committed
                - data is securely store in a local database
            - modified
                - file has been changed, but not committed
            - staged
                - flagged a file's changed versio to be committed in the next snapshot

[< back](README.md)