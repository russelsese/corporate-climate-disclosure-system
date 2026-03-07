sequenceDiagram
    autonumber

    actor Owner as Business Owner
    actor Delegate as Delegate
    participant Reviewers as ESG / Risk / Finance Reviewers
    participant Approver as Executive Approver
    participant Board as Board
    participant Secretariat as Company Secretary

    Owner->>Delegate: Delegate preparation work
    Delegate->>Owner: Return completed draft and evidence
    Owner->>Reviewers: Submit business unit disclosure
    Reviewers-->>Owner: Review and request updates if needed
    Owner->>Approver: Submit for executive approval
    Approver-->>Owner: Approve or reject
    Approver->>Board: Submit final pack
    Board-->>Approver: Approve or request changes
    Board->>Secretariat: Authorise final submission
    Secretariat->>Secretariat: Lodge, publish, and archive