---

title: Multi-channel data driven, real-time fraud determination system for electronic payment cards
abstract: Exemplary embodiments for detecting electronic payment card fraud include receiving real-time payment card transaction data from ingress channels and an egress channels of at least one payment card system through a first application programming interface (API); generating transactional profiles for each of at least payment cards, the ingress channel, the egress channels, and funding sources of the payment cards; in response to receiving transaction data for a current payment card transaction, evaluating the transaction data using a predictive algorithm that compare the transaction data to the transactional profiles to calculate a probabilistic fraud score for the current transaction; evaluating the probabilistic fraud score and the current transaction data based on a set of rules to generate a recommendation to approve, decline or review the current transaction; and transmitting the recommendation back to the payment card system via a second API.
url: http://patft.uspto.gov/netacgi/nph-Parser?Sect1=PTO2&Sect2=HITOFF&p=1&u=%2Fnetahtml%2FPTO%2Fsearch-adv.htm&r=1&f=G&l=50&d=PALL&S1=08738529&OS=08738529&RS=08738529
owner: Wal-mart Stores, Inc.
number: 08738529
owner_city: Bentonville
owner_country: US
publication_date: 20120715
---
This application claims the benefit of provisional Patent Application Ser. No. 61 508 486 filed Jul. 15 2011 incorporated herein by reference.

A stored value card refers to monetary value stored on a card not in an externally recorded account while with a prepaid card money is on deposit with an issuer similar to a debit card. That is the term stored value card means the funds and or data are physically stored on the card while with a prepaid card the data is maintained on computers affiliated with the card issuer. Another difference between stored value SV cards and prepaid PP referred to collectively as SV PP or electronic payment cards is that prepaid debit cards are usually issued in the name of individual account holders while stored value cards are usually anonymous.

Stored Value Pre Paid cards allow for anonymous loading of monetary value on these cards by fraudsters through stolen financial instruments and cash at multiple channels or entry points namely web mobile agents and other point of sale mechanisms. Currently all of these channels operate independently and without knowledge of transactional activities on other channels. Electronic payment cards allow for multiple channels of disbursements or exit points namely physical point of sale locations web ATM and mobile.

One problem with electronic payment cards is that fraud perpetrators can avoid detection by loading multiple smaller value stored value pre paid cards simultaneously on different channels for entry into the system. In addition money movement from a compromised entry source to a fraudulent SV PP card is very rapid. Further money movement between countries is very easy and rapid making recapture of fraudulent funds more difficult based on the plurality of regulations and jurisdictions that can apply.

Accordingly it would be desirable to provide an improved method for detecting electronic payment card fraud.

Exemplary embodiments provide methods and systems for detecting electronic payment card fraud. Aspects of the exemplary embodiments include receiving real time payment card transaction data from ingress channels and an egress channels of at least one payment card system through a first application programming interface API generating transactional profiles for each of at least payment cards the ingress channel the egress channels and funding sources of the payment cards wherein a first type of transactional profile include a first profile comprising a network graph of links between the ingress channels the egress channels the payment cards and any users of the payment cards and geo location identities associated with the payment cards in response to receiving transaction data for a current payment card transaction evaluating the transaction data using a predictive algorithm that compare the transaction data to the transactional profiles to calculate a probabilistic fraud score for the current transaction evaluating the probabilistic fraud score and the current transaction data based on a set of rules to generate a recommendation to approve decline or review the current transaction and transmitting the recommendation back to the payment card system via a second API.

The exemplary embodiments relate to methods and systems for detecting electronic payment card fraud. The following description is presented to enable one of ordinary skill in the art to make and use the invention and is provided in the context of a patent application and its requirements. Various modifications to the exemplary embodiments and the generic principles and features described herein will be readily apparent. The exemplary embodiments are mainly described in terms of particular methods and systems provided in particular implementations. However the methods and systems will operate effectively in other implementations. Phrases such as exemplary embodiment one embodiment and another embodiment may refer to the same or different embodiments. The embodiments will be described with respect to systems and or devices having certain components. However the systems and or devices may include more or less components than those shown and variations in the arrangement and type of the components may be made without departing from the scope of the invention. The exemplary embodiments will also be described in the context of particular methods having certain steps. However the method and system operate effectively for other methods having different and or additional steps and steps in different orders that are not inconsistent with the exemplary embodiments. Thus the present invention is not intended to be limited to the embodiments shown but is to be accorded the widest scope consistent with the principles and features described herein.

The exemplary embodiments provide methods and systems for detecting electronic payment card fraud for multi channel funds in and funds out electronic payment card programs. The exemplary embodiment will be explained in terms of an electronic payment card that is intended to include stored value cards and pre paid cards. However in some embodiments electronic payment cards may also include credit and debit cards.

The fraud monitoring method and system of the exemplary embodiment allow for real time monitoring of all funds loaded onto an electronic payment card all fund movement within an electronic payment card system and all fund exits out of the electronic payment card system. One aspect of the exemplary embodiment is the ability of the fraud detection system to create a network of linked individuals channels electronic payment cards geographies and time to describe fraudulent behavior and to use this network to assign probabilities of a current transaction being a fraudulent transaction. Based on these probabilities a recommendation is created and sent back to the payments system through a recommendation application programming interface API to approve decline or review the transaction.

Real time monitoring of funds moving into and exiting an electronic payment card across multiple channels may be accomplished with the use of a real time feedback events that notify the fraud detections system of known fraud behavior and b self learning fraud prediction algorithms that use this real time feedback to modify the algorithms to account for current patterns in fraud behavior. The fraud detection system dynamically updates and reflects current fraud trends for detecting patterns of use as wells as tracks fund movements to electronic payment cards. The fraud detection system uses payment card transaction data from conventional payments systems to build profiles and networks of users payment cards ingress and egress channels and funding sources across multiple dimensions.

The system has abilities to track money through each point of transfer through the network and represent it as a visual graphic allowing for enhanced fraud monitoring and detection. The fraud detection system evaluates the network created by the transactional ingress and egress channel links to the electronic payment cards as well as the adjoining networks to assess fraud risk of the electronic payment cards. The system has abilities to use past history of suspicious behavior in the form of probabilistic and deterministic negative files to generate recommendation to decline or review a current card transaction when strong links are established between an incoming user card with those on negative files. The fraud detection system also may evaluate every transaction in an electronic payment card system in real time using internal and external data to predict fraud risk with a dynamic rules engine and or predictive models to recommend a decision to approve decline review a card transaction. Internally created data and externally sourced data may be merged to validate geo location phone numbers addresses devices and the like.

The egress channels . may include using the electronic payment card on the internet Web . to buy easily fenceable goods or digital goods using mobile phones . to move money to other accounts and or buy digital goods using ATM . to withdraw funds as cash using the electronic payment card at a Point of Sale . venues to buy fenceable goods and withdraw funds as cash.

Each of the channels . and . and funding mechanisms are distinctly different. Each of the channels . and . and funding mechanisms have distinct fraud prevention needs that address matching individual fraud vulnerabilities. In current payments systems the fraud system runs on disparate rails with each channel and funding source reviewing fraud risk as is appropriate to itself. Such a non aggregated system does not allow for a wider view of fraud risk and propagates a fragmented fraud prevention effort.

According to the exemplary embodiment a dynamic fraud detection system is provided that brings together all incoming outgoing and intra network electronic payment transactions in real time through a data transfer API. The data transfer API allows payments systems from various entities such as banks to transmit data into the fraud system in real time in order to reference internal data sources such as historical transactional profiles transaction data including transaction specific data as well as geo location characteristics and external data sources to evaluate the holistic fraud risk of the electronic payment card as well as each channel and funding mechanism. After each transaction is completely evaluated the fraud detection system sends a response that contains a score and a recommendation to approve decline or review the transaction back to the originating system through a recommendation API. Review of the transaction may require manual review of the transaction by a customer service agent and or a call to the electronic payments system.

Fraud evaluation and detection may begin by receiving real time payment card transaction data from ingress channels and egress channels from at least one payment card system through the ingress and egress transaction data transfer API ..

This is followed by the fraud monitoring component . generating and or updating transactional profiles for each of at least payment cards the ingress channel the egress channels funding sources of the payment cards and users of the payment cards. The transactional profiles may be used to evaluate usage patterns and in one embodiment are stored as the network graph data . the channel profile data . the transactional profile data . the funding instrument data . and the external data verification database ..

In one embodiment the fraud monitoring component . may generate two types of transactional profiles for each of the electronic payment card the ingress channels the egress channels and the funding source. The first type of transactional profile may comprise a network graph of links between the ingress channels the egress channels the payment cards any users of the payment cards and geo location identities associated with the payment cards. The network graph may be stored as the network graph data ..

The second type of transactional profile may comprise a series of transactional usage patterns at different time intervals for each of the payment cards the ingress channels the egress channels and the funding sources. The transactional usage patterns may be stored as the channel profile data . the transactional profile data . and the funding instrument data .. In addition to this data the fraud management system . may invoking API calls to populate the external data verification database . with data retrieved from external sources that are used to verify geo location e.g. internet protocol IP addresses phone numbers and addresses associated with the current transaction.

In one embodiment the fraud monitoring component . may comprise three main modules namely a network graph module a profile module and external data retrieval module not shown . The network graph module may be configured to create the network graph data .. The profile module may be responsible for creating the transactional profiles including the channel profile data . transactional profile data . and the funding instrument data .. External data retrieval module may be responsible for making the API calls necessary for retrieving the external data used to populate the external verification database .. All three modules may be configured to facilitate fast traversal through the data allow for new data elements to be added without schema changes and accommodate sparse data structures. The three modules may be meta data driven and may have an embedded rules language to build and update relationships and profiles.

After the appropriate transactional profiles are created for the transaction data received from the payments system for a current payment card transaction the transaction data is processed by the fraud scoring component .. In response to receiving transaction data for the current payment card transaction the fraud scoring component . uses a set of predictive algorithms that compare the transaction data to the transactional profiles to calculate a probabilistic fraud score for the current transaction.

In one embodiment the fraud scoring component . has the capability to pull data from the network graph data . the channel profile data . the transactional profile data . the funding instrument data . and from the external data verification API . to compute predictive probabilistic scores.

The fraud scoring component . may be configured to utilize multiple predictive algorithms in general as well as within a given use case. The predictive algorithms may include but are not limited to regression decision trees neural networks random forest and genetic algorithms. The result of the fraud scoring component . is a probabilistic score assigned to a transaction and or to the parties involved in the transaction. The fraud scoring component . is designed to be self learning with the ability to incorporate new fraudulent behaviors into the predictive algorithms.

Next the fraud recommendation component . evaluates the probabilistic fraud score and the current transaction data based on a set of rules and generates a recommendation to approve decline or review the current transaction. The fraud recommendation component . then transmits the recommendation back to the payment card system via the recommendation APIs ..

The fraud recommendation component . may utilize a rules language to build and deploy cutoff strategies further refining the probabilistic score to minimize false positive and false negative incidences. The fraud recommendation component . similar to the fraud scoring system . has access to all other systems and data within the larger fraud detection system . The fraud recommendation component . may have self discovery capabilities that allow it to discover and use new data elements without schema and code changes due to the meta data driven nature of the system. The fraud recommendation component . packages the probabilistic score along with a recommendation to approve decline or review that is sent to the payments system through the transactions recommendation API .. The recommendation can be embedded as part of a response back to an incoming transaction request received over the data transfer API or can be posted asynchronously to a pre defined location.

One aspect of the exemplary embodiment is the ability of the fraud detection system to communicate with one or more payment systems . In one embodiment the ingress egress transaction data transfer API . contains two components a fixed component that allows for uniformity of sending data across multiple channels and a flexible component that allows each channel to send data that is unique and relevant to that channel. The ingress egress transaction data transfer API . may use JavaScript Object Notation JSON to define the payload.

In one embodiment the ingress egress transaction data transfer API . can be one of three versions 1 Fire and Forget used when a sending entity does not expect a response but is merely sending the message to advise the fraud detection system of a change in status of the payment card 2 Synchronous used when a sending entity is expecting a recommendation as part of the response back to the sending entity and 3 Asynchronous used when a sending entity is expecting a recommendation but not as part of the response back. An asynchronous response is posted back to the sending entity s pre designated location.

Although the ingress and egress transaction data transfer API . the fraud monitoring component . the fraud scoring component . the fraud recommendation component . and the transaction recommendation API . are shown as separate components the functionality of each may be combined into a lesser or greater number of modules components.

In addition it should be understood the fraud detection system may be implemented as a web service that communicates with one or multiple payments systems over the internet through respective servers not shown . Further the fraud monitoring component . the fraud scoring component . and the fraud recommendation component . may run on one or more servers or on any type of computers that have memory and processors.

The servers and or computers comprising the fraud detection system may include hardware components of typical computing devices not shown including one or more processors input devices e.g. keyboard pointing device microphone for voice commands buttons touchscreen etc. and output devices e.g. a display device speakers and the like . The servers and computers may include computer readable media e.g. memory and storage devices e.g. flash memory hard drive optical disk drive magnetic disk drive and the like containing computer instructions that implement the functionality disclosed when executed by the processor s . The server and or the computers may further include wired or wireless network communication interfaces for communication.

The funds moving on to an electronic payment card may happen simultaneously across multiple channels and multiple funding sources. The Funds In fraud system process looks at all ingress channels simultaneously and evaluates fraud risk on both individual electronic payment cards as well as the individual ingress channel.

According to the exemplary embodiment the funds in process looks at all ingress points simultaneously as well as all funding sources funding in to a single point allowing for capturing fraud at both an electronic payment card level as well as the individual ingress point.

The funds out process evaluates at all egress points simultaneously allowing for capturing fraud at both an electronic payment card level as well as the individual egress point.

A method and system for detecting electronic payment card fraud has been disclosed. The present invention has been described in accordance with the embodiments shown and there could be variations to the embodiments and any variations would be within the spirit and scope of the present invention. For example the exemplary embodiment can be implemented using hardware software a computer readable medium containing program instructions or a combination thereof. Software written according to the present invention is to be either stored in some form of computer readable medium such as a memory a hard disk or a CD DVD ROM and is to be executed by a processor. Accordingly many modifications may be made by one of ordinary skill in the art without departing from the spirit and scope of the appended claims.

