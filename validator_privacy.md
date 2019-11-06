# Anonymity networks for Proof of Stake Protocols

- [On Privacy notions in ACNs](https://petsymposium.org/2019/files/papers/issue2/popets-2019-0022.pdf)


## Design goals for ACNs applied to Proof of Stake networks
- How to ensure both low latency and low bandwith?
    - Given that the anonymity trilemma only states that you can choose 2 from {"Strong Anonymity", "Low Latency", "Low Bandwith"}, this question is better phrased as "What kind of anonymity guarantees can we get in such a network"
    - Answer: Can't get strong anonymity in the presence of a global passive adversary if low bandwidth overhead and low latency overheard are priortized.
- Can currently proposed and in-use anonymity networks be used for PoS protocols?
    - Maybe?
    - Some of these networks such as Tor and I2P may not be a good fit due to latency, bandwidth and scale issues. However, onion/garlic routing might be worth exploring. 
- Can we attribute faults in anonymity networks? In other words, can we still guarantees the same cryptoeconomic security under these networks?
    - Due to the properties of PoS, we need to be able to slash misbehaving nodes.
- Alternatively, can we provide "decent" anonymity to PoS networks in which the consensus protocol itself doesn't take into acccount anonymity? How can we quantify this?
    - What kind of metadata leakage do we get in this case?
- How does anonymity better/worsen the guarantees of proof of stake networks?
    - How do we maintain BFT properties?
    - What are the tradeoffs between consistency and availability?
        - Most ACNs favor availability and uptime more than consistency? What effect does this have on PoS protocols favoring consistency over availability?
- What threat model are we considering?
    - Global passive adversary
    - Global active adversary
    - etc

## Requirements
- Low Latency
- Low Bandwidth
- Long-lasting identities
- Weakly anonymous
- Accountable?
- sender unlinkability, etc

## Kinds of attacks validators are susceptible to without anonymity

## Threat/Attacker model


## Why can't we use the current state of the art?
Broadly, can separate techniques used to add network layer anonymity to blockchains:

 - Cryptographic methods
     - Can guarantee strong anonymity
     - Computationally expensive
     - Cryptographic proofs to ascertain to the security of the scheme
     - Work based on well-studied anonymization techniques
         - Onion-routing, mixnets, etc.
 - Topological methods
     - Guarantees weaker anonymity than crytopgraphic methods
     - Easier to deploy
     - Dandelion/Dandelion++
         
- Look at the current state of the art as it relates to the requirements
    - Tor
        - Torsocks
        - Low latency
        - Low bandwidth
        - Has been attacked in practice
            - Might make network more susceptible to certain kinds of timing attacks and MITM attacks
