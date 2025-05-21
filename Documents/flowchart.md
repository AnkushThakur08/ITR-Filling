```mermaid
graph TD;
  A[User Lands on Website] --> B[Login / Signup]
  B -->|New User| C[Register & Verify OTP]
  B -->|Existing User| D[Login]
  C --> D

  D --> E[Dashboard]
  E --> F[Upload Documents]
  E --> G[View Past ITRs]
  E --> H[Make Payment]
  E --> I[Check Status]

  F -->|Upload Complete| J[Admin Receives Data]
  J --> K[Admin Reviews ITR]
  K -->|Approved| L[ITR Filed & Confirmation Sent]
  K -->|Rejected| M[Request for Correction]

  H -->|Payment Success| N[Generate Invoice]
  H -->|Payment Failed| O[Retry Payment]

  L --> P[User Gets Notification & Email]
  M --> E[User Re-uploads Documents]
  G --> Q[Download Previous ITRs]
  I --> R[Track ITR Filing Status]

  subgraph Admin Panel
    J
    K
    L
    M
  end


