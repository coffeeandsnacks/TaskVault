# TaskVault - Grizzlython Hackathon Submission 2023
TaskVault is a decentralized freelancing platform for Solana and the Web3-Space. It aims to be the one-stop-shop for aspiring web3-freelancers to find a web3-job the web3-way. It is best understood in terms of its components:
- TaskVault is a matching service for finding and hiring Web3-Talent.
- TaskVault is a secure escrow service for handling stablecoin-payments related to Freelancing-Jobs.
- TaskVault is a smart arbitration system for handling disputes related to Freelancing-Jobs. 

TaskVault is being built, because the status quo of freelancing in web3 is clearly broken. Today, freelancers must establish a high-level of trust with the client first before even being able to work, because there is no easy way to handle escrow payments yet. And existing (web2) freelancing-platforms like upwork or fiverr, do not support stable-coins and charge really high fees (10-25%).

# Demo
https://user-images.githubusercontent.com/94404088/225144954-061368ad-fca7-41dd-8924-a96968b6b277.mp4


# Technical Design
Checkout our Docs at 
https://taskvault.simple.ink/welcome-to-our-documentation-051eb7c41cd141dda89370650f7cfe97



<img width="1245" alt="Client-Process" src="https://user-images.githubusercontent.com/94404088/225141513-fb857704-2604-4f3a-976c-6e1486cae231.png">



<img width="1247" alt="Freelancer-Process" src="https://user-images.githubusercontent.com/94404088/225141833-c8ac74fb-317c-47c7-8fc4-ee909bb13a00.png">



<img width="318" alt="Dispute Resolution" src="https://user-images.githubusercontent.com/94404088/225141920-1e26e99b-576a-4afe-aff2-a752030800d8.png">





# Smart Contract Specification
Features:
1. Profile Creation: Freelancers and clients must be able to create their profiles on the platform. These profiles will contain information about the user, including their skills, work experience, and portfolio. The profiles will be stored on IPFS, ensuring that they are easily accessible and tamper-proof.

2. Escrow Logic: The smart contract will include an escrow logic, allowing clients to deposit the money before the job begins. This ensures that the freelancer is paid for their work, even if the client is dissatisfied with the results. The funds will be held in a 2-of-3 multisig, where the client, freelancer, and an arbitrator will have a say in case of a dispute. Freelancers will also be able to lock some of their own money in case of cheating, protecting themselves from clients who refuse to pay.

3. Job Creation: Clients will be able to create jobs, including the job description, the amount they are willing to pay, and the deadline. Freelancers will be able to browse these job postings and submit proposals if they are interested.

4. Proposal Submission: Freelancers will be able to submit proposals to clients for specific jobs. These proposals will include a description of the work they will do, the time it will take, and the price they are willing to accept.

5. Job Acceptance: Once a proposal has been submitted, the client will review it and decide whether to accept or reject it. If they accept the proposal, the job will be considered awarded to the freelancer, and the escrow logic will be initiated.

6. Work Completion: Freelancers will complete the work within the agreed timeframe and submit it to the client. The client will review the work and either approve it or request changes. If the work is not approved, the freelancer will be required to make revisions until the work meets the client's satisfaction. If after a reasonable number of revisions the work is still not approved, the funds will stay locked in the multisig.

7. Dispute Resolution: In case of a dispute between the client and the freelancer, a third-party mediator will be called in to facilitate the resolution. The mediator will make a suggestion for how to resolve the dispute, and both parties will have to agree to the proposed solution. If both parties cannot agree on the proposed solution, an arbitrator will be called in to make the final decision. The arbitrator will have access to the multisig and will decide to whom the locked funds belong, based on the terms of the contract and the details of the dispute.

8. Platform Fees: The platform will charge a fee for each job posted and completed. This fee will be deducted from the amount paid by the client and paid to the platform.

 
