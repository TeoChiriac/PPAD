# PPAD
PPAD is Privacy-preserving group-based advertising for online social networks (OSN). In a nutshell, it enables performing boolean queries over a group of encrypted sets of attributes. The encrypted sets of attributes are outsourced to the OSN and the entire computation is carried out by two non-colluding servers. Servers receive any plaintext query from an advertiser, run the query over the encrypted sets, and find the matched sets i.e., users. The reference and the link to the paper are given below.

Boshrooyeh, Sanaz Taheri, Alptekin Küpçü, and Öznur Özkasap. "PPAD: Privacy-preserving group-based advertising in online social networks." 2018 IFIP Networking Conference (IFIP Networking) and Workshops. IEEE, 2018.

link: https://www.researchgate.net/profile/Alptekin_Kuepcue/publication/332676013_PPAD_Privacy_Preserving_Group-Based_ADvertising_in_Online_Social_Networks/links/5cd948fb458515712ea6d56a/PPAD-Privacy-Preserving-Group-Based-ADvertising-in-Online-Social-Networks.pdf

# Implementation 
This repo contains the proof-of-concept implementation of PPAD in Java programming language.

PPAD has four main players, namely, users (data owners), advertisers (queriers), and two servers. Each role and its associated actions are modeled inside a separate java class. 

Server.java and PSP.java represent the two servers of PPAD. The user entity is modeled in Profile.java whereas the advertiser is realized in Advertiser.java .
Group.java allows to bind a group of profiles together (the notion of group is used while performing the matching procedure, for more details please check the paper). 
The sets of attributes are modeled using Bloom filters whose implementation is given in BloomFilter.java. 
For the sake of demo, DB.java contains methods necessary for generating synthetic profiles (i.e., attribute sets) and advertising request (i.e., queries).

