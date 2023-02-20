# Secure Software Requirements

### 1. Confidentiality Requirements

- What are these requirements aimed at?
    > Confidentiality requirements are aimed at providing protection against data disclosure. So in simple words, to reduce the risk of having confidential/sensitive documents public (make them accessible for everyone)
- When should these requirements be met and why?
    > These requirements should be met in each SDLC phase, and each part of the application, where we deal with confidential/sensitive data (the whole data lifecycle) until data becomes non longer private/valuable/confidential
    >
    > We distinguish 3 phases in the data lifecycle:
    >>_in transit_:
    >>
    >> "When the data are transmitted over unprotected networks"
    >
    >>_in processing_:
    >>
    >> "When the data are held in computer memory or media for processing"
    >
    >>_in storage_:
    >>
    >> "When the data are at rest, within transactional systems as well as nontransactional systems including archives"
- How to understand which data is confidential/sensitive?
    > In general, data can be classified as public and nonpublic.
    >
    > If the data contains any information regarding health, finances, identity, or any information valuable for the business (e.g. acquisitions, company strategy), so data that can be overused or causes damage, it should be determined as nonpublic, in other words, as confidential/sensitive.
    >
    > More granular classification can be provided by company policy (eg. Strictly Confidential, Restricted, Business Use Only, Public)
- What are the approaches to meeting these requirements? (encryption, hashing, masking)
    >The two common forms of confidentiality protection mechanisms:

    ```mermaid
        flowchart TD
        A[Confidential controls] --- B & C[Masking]
        B[Secret writing] --- D[Covert] & E[Overt]
        D --- F[Steganography] & G[Digital watermarking]
        E --- H[Encryption] & I[Hashing]
    ```

    >_Masking_
    >
    > "is a weaker form of confidentiality protection mechanism in which the original information is either asterisked or X’ed out. You may have noticed this in input fields that take passwords. This is primarily used to protect against shoulder surfing attacks, which are characterized by someone looking over another’s shoulder and observing sensitive information"
    
    >_Secret writing_
    >
    > "is a protection mechanism in which the goal is to prevent the disclosure of information deemed secret"
    >
    >>_Covert_
    >>
    >> "A technique of secret writing to hide information within itself or in some other media or form"
    >
    >>>_Steganography_
    >>>
    >>> "is more commonly referred to as invisible ink writing and is the art of camouflaging or hidden writing, where the information is hidden and the existence of the message itself is concealed"
    >
    >>>_Digital watermarking_
    >>>
    >>> is the process of embedding information into a digital signal. These signals can be audio, video, or pictures. Digital watermarking can be accomplished in two ways: visible and invisible. In visible watermarking, there is no special mechanism to conceal the information, and it is visible to plain sight. This is of little consequence to us from a security standpoint. However, in invisible watermarking, the information is concealed within other media and the watermark is used to uniquely identify the originator of the signal, thereby making it possible for authentication purposes as well, besides confidentiality protection. Invisible watermarking is, however, mostly used for copyright protection, deterring and preventing unauthorized copying of digital media. Digital watermarking can be accomplished using steganographic techniques as well
    >
    >>_Overt_
    >>
    >> commonly referred to as cryptography, includes encryption and hashing
    >
    >>>_Encryption_
    >>>
    >>> uses a bidirectional algorithm in which humanly readable information (referred to as clear text) is converted into humanly unintelligible information (referred to as cipher text). The inverse of encryption is decryption, the process by which cipher text is converted into plain text
    >
    >>>_Hashing_
    >>>
    >>> is a one-way function where the original data or information that needs protection is computed into a fixed length output that is indecipherable. The computed value is referred to as a hash value, digest, or hash sum. The main distinction between encryption and hashing is that, unlike in encryption, the hashed value or hashed sum cannot be converted back to the original data and hence the one-way computation
- Examples
    > “Personal health information must be protected against disclosure using approved encryption mechanisms.”
    > 
    >“Password and other sensitive input fields need to be masked.”
    >
    >“Transport layer security (TLS) such as Secure Socket Layer must be in place to protect against insider man-in-the-middle (MITM) threats for all credit card information that is transmitted.”
    >
    >“The use of nonsecure transport protocols such as File Transfer Protocol (FTP) to transmit account credentials in the clear to third parties outside your organization should not be allowed.”
    >
    >“Log files must not store any sensitive information as defined by the business in humanly readable or easily decipherable form.”

### 2. Integrity Requirements

- What are these requirements aimed at?
    > ...
- What are the approaches to meeting these requirements? (input validation, parity bit checking, CRC, hashing)
    > ...
- Examples
    > ...

### 3. Availability Requirements

- What are these requirements aimed at?
    > ...
- What are the metrics that allow you to track the fulfillment of these requirements? (Maximum Tolerable Downtime and Recovery Time Objective; they should be defined in SLA)
    > ...
- Examples
    > ...

### 4. Authentication Requirements

- What are these requirements aimed at?
    > ...
- 2FA is the implementation of which security design principle?
    > ...
- Most common auth types
  - cons and pros
    > ...
  - what cases each of them is suitable for and why?
    > ...

### 5. Authorization Requirements

- What are these requirements aimed at?
    > ...
- What CRUD is?
    > ...
- Access control models (description, cons and pros):
  - Discretionary Access Control (DAC)
    > ...
  - Non-Discretionary Access Control (NDAC)
    > ...
  - Mandatory Access Control (MAC)
    > ...
  - Role-Based Access Control (RBAC)
    > ...
  - Resource-Based Access Control
    > ...
- Examples
    > ...

### 6. Accountability Requirements

- What are these requirements aimed at?
    > ...
- Logging:
  - Describe the format (who/what/where/when)
    > ...
  - What events need to be logged? (failed attempts, successful attempts, limits exceeding, etc.)
    > ...
- Examples
    > ...

### 7. Session Management Requirements

- What are these requirements aimed at?
    > ...
- What are the approaches to meeting these requirements?
    > ...
- Examples
    > ...

### 8. Errors & Exception Management Requirements

- What are these requirements aimed at?
    > ...
- What are the approaches to meeting these requirements?
    > ...
- Examples
    > ...

### 9. Configuration Parameters Management Requirements

- What are these requirements aimed at?
    > ...
- What are the approaches to meeting these requirements?
    > ...
- Examples
    > ...

### 10. Operational Requirements

- What are these requirements aimed at?
    > ...
- What are the approaches to meeting these requirements?
    > ...
- Examples (backups, patching, secret management, incident management)
    > ...

### 11. Deployment Environment Requirements

- What are these requirements aimed at?
    > ...
- What are the approaches to meeting these requirements?
    > ...
- Examples
    > ...

### 12. Protection Needs Elicitation (PNE) Techniques

- Brainstorming
    > ...
- Surveys (Questionnaires and Interviews)
    > ...
- Policy Decomposition
    > ...
- Data Classification
    > ...
- Subject-Object Matrix
    > ...
- Use Case & Misuse Case Modeling
    > ...
