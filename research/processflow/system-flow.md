sequenceDiagram
    autonumber

    actor Owner as Data Owner / Department Lead
    actor Delegate as Delegate / Analyst
    participant ESG as Sustainability Team
    participant Risk as Risk & Compliance
    participant Finance as Finance Team
    participant Exec as Executive Approver
    participant Board as Board / Committee
    participant CompanySec as Company Secretary
    participant System as Climate Disclosure Workflow System
    participant Regulator as ASIC / Annual Report Publication

    Owner->>System: Create disclosure task / reporting submission
    System->>Owner: Show required sections, due dates, evidence checklist

    alt Owner delegates preparation
        Owner->>System: Assign task to Delegate
        System->>Delegate: Notify delegated preparer
        Delegate->>System: Upload data, commentary, evidence
        Delegate->>Owner: Submit draft back for owner review
        Owner->>System: Confirm business section is ready
    else Owner prepares directly
        Owner->>System: Upload data, commentary, evidence
    end

    System->>ESG: Route submission for sustainability review
    ESG->>System: Review completeness, methodology, disclosures

    alt ESG review failed
        ESG-->>Owner: Return with comments / corrections required
        Owner->>System: Revise or re-delegate updates
    else ESG review passed
        ESG->>System: Approve sustainability review
    end

    System->>Risk: Route for risk and compliance review
    Risk->>System: Review regulatory alignment, risk statements, controls

    alt Risk review failed
        Risk-->>Owner: Request correction / clarification
        Owner->>System: Resubmit updated content
        System->>ESG: Recheck if material changes made
    else Risk review passed
        Risk->>System: Approve compliance review
    end

    System->>Finance: Route for finance sign-off
    Finance->>System: Review financial consistency and annual report alignment

    alt Finance review failed
        Finance-->>Owner: Return for correction
        Owner->>System: Update figures / narrative
        System->>ESG: Revalidate disclosure
        System->>Risk: Revalidate compliance if needed
    else Finance review passed
        Finance->>System: Approve finance review
    end

    System->>Exec: Request executive approval

    alt Executive delegates approval authority
        Exec->>System: Delegate approval to authorised approver
        System->>Delegate: Notify delegated approver
        Delegate->>System: Review and approve within delegation limit
    else Executive reviews directly
        Exec->>System: Review disclosure pack
    end

    alt Executive rejects
        Exec-->>Owner: Return for revision
        Owner->>System: Update submission
        System->>ESG: Restart review cycle
    else Executive approves
        Exec->>System: Executive sign-off complete
    end

    System->>Board: Submit final disclosure for board / committee approval
    Board->>System: Review final report, risks, targets, declarations

    alt Board requests changes
        Board-->>Exec: Request amendments
        Exec-->>Owner: Direct revisions
        Owner->>System: Update disclosure pack
        System->>ESG: Re-run approvals as needed
    else Board approves
        Board->>System: Final board approval
    end

    System->>CompanySec: Prepare submission and publication pack
    CompanySec->>System: Confirm approvals, minutes, declarations, version control
    CompanySec->>Regulator: Lodge with annual reporting / publish disclosure
    System->>Owner: Mark submission as completed and archived