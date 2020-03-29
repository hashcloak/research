ZkStudyClub: Polynomial Commitments with Justin Drake pt. 2
- [cryptographic ingredient for universal SNARKs](https://www.youtube.com/watch?v=BfV7HBHXfC0&feature=youtu.be)

Sonic 
- [Introducing Sonic: A Practical zk-SNARK with a Nearly Trustless Setup](https://www.benthamsgaze.org/2019/02/07/introducing-sonic-a-practical-zk-snark-with-a-nearly-trustless-setup/)
- [Sonic: Zero-Knowledge SNARKs from Linear-Size Universal and Updatable Structured Reference Strings](https://eprint.iacr.org/2019/099.pdf)
- [Sonic MPC implementation by Matter Labs](https://github.com/matter-labs/alpha_line)

SuperSonic
- [Polynomial Commitments and Evaluation Proofs from Groups of Unknown Order](https://www.youtube.com/watch?v=YZ0w-cZTQ-M&list=PLcIyXLwiPilWvjvNkhMn283LV370Pk5CT&index=7)
<br>Given a polynomial commitment schemes from groups of unknown order,instantitate this with class groups, then will  get transparent setup 
and  a few other nice properties . Apply it with Sonic, then will result in something called SuperSonic.
It's a trustless setup SNARK with *log(n)* proof size and *log(n)* verification, quasi-linear prover time + preprocessing, 
as well as 24 kb proof size for 1 million gate circuits.


Marlin  
- [Marlin: Preprocessing zkSNARKs with Universal and Updatable SRS](https://eprint.iacr.org/2019/1047.pdf)
- [Marlin: One of the fastest snarks in the ocean](https://www.benthamsgaze.org/2019/09/19/a-marlin-is-one-of-the-fastest-snarks-in-the-ocean/)

PLONK 
- [Ignition: Trusted Setup MPC Ceremony for PLONK (planned October 2019)](https://medium.com/aztec-protocol/aztec-announcing-our-ignition-ceremony-757850264cfe)
- [PLONK: Permutations over Lagrange-bases for Oecumenical Noninteractive arguments of Knowledge](https://eprint.iacr.org/2019/953.pdf)
- [Understanding PLONK](https://vitalik.ca/general/2019/09/22/plonk.html)

DARK 
- [Transparent SNARKs from DARK Compilers](https://eprint.iacr.org/2019/1229.pdf)

MIRAGE  
- [MIRAGE: Succinct Arguments for Randomized Algorithms with Applcations to Universal zk-SNARKs](https://eprint.iacr.org/2020/278.pdf)

<big>**Thoughts**<big>  
Three flavours of general-purpose snarks:    
- Powers of tau  
  generating and safely disposing of toxic waste 
  used by [Sonic](https://eprint.iacr.org/2019/099.pdf) and [PLONK](https://eprint.iacr.org/2019/953.pdf)  
- FRI-based 
  [STARKs by STARKWARE](https://eprint.iacr.org/2018/046.pdf)  
- RSA or class group 
  [Supersonic](https://eprint.iacr.org/2019/1229.pdf)
  
Trade-offs between different options:  
- With *updatable* universal setups:  
  [Sonic](https://eprint.iacr.org/2019/099.pdf)  
  
- With *non-updatable* universal setups:  
  [AuroraLight](https://eprint.iacr.org/2019/601.pdf)
  [Hyrax](https://eprint.iacr.org/2019/1132.pdf)
  [Libra](Libra: Succinct Zero-Knowledge Proofs with Optimal ProverComputation)

- With transparent setups:  
  [Fractal](https://eprint.iacr.org/2019/1076.pdf),
  [Halo](https://eprint.iacr.org/2019/1021.pdf),
  [Supersonic](https://eprint.iacr.org/2019/1229.pdf),
  [Spartan](https://eprint.iacr.org/2019/550.pdf),  
  Adcantages : Relies on common reference string, public ,no toxic waste.  
  Disadvantages : big proof size .  
- Performance:  
  prover time and verifier time  
  
  
Universality for a polynomial commitment scheme :   
- language-specific: a polynomial commitment only proves one language
- Speed up by multi-opening solution,introduced by [Efficient polynomial commitment schemes formultiple points and polynomial](https://eprint.iacr.org/2020/081.pdf)  

Discussion of universal succintness:
- [universal arguments]:(https://eprint.iacr.org/2014/580.pdf),page 27,needs future improvements.

Definition of soundness :
- standard definition of special soundness : Interact arbitrarily with an update oracle to set the SRS .
- [interactive definition by Sonic](https://eprint.iacr.org/2019/099.pdf),page 5: given an initial one and update in one-shot fashion .

Discussion of security models and hardness assumptions :
- [updatable knowledge soundness](https://smeiklej.com/files/crypto18.pdf), page 22  
- [KEA assumptions](https://smeiklej.com/files/crypto18.pdf),page 18  

Discussion of security and efficiency:
- [Proof of security](https://eprint.iacr.org/2014/580.pdf),page 23  
  construct circuits of extraction,then prove it with satisfied properties .  
  enhance efficiency by applying "universal succintness"  



