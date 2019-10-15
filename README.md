# DeepSignDB

## **INSTRUCTIONS FOR DOWNLOADING DeepSignDB**

1. [Download license agreement](http://atvs.ii.uam.es/atvs/licenses/DeepSignDB_License.pdf), send by email one signed and scanned copy to [**atvs@uam.es**](mailto:atvs@uam.es) according to the instructions given in point 2.
2. Send an email to [**atvs@uam.es**](mailto:atvs@uam.es), as follows:

    _Subject:_ **[DATABASE download: DeepSignDB]**

    Body: Your name, e-mail, telephone number, organization, postal mail, purpose for which you will use the database, time and date at which you sent the email with the signed license agreement.

1. Once the email copy of the license agreement has been received at ATVS, you will receive an email with a username, a password, and a time slot to download the database.
2. [Download the database](http://atvs.ii.uam.es/atvs/intranet/free_DB/DeepSignDB), for which you will need to provide the authentication information given in step 4. After you finish the download, please notify by email to [**atvs@uam.es**](mailto:atvs@uam.es) that you have successfully completed the transaction.
3. For more information, please contact: [**atvs@uam.es**](mailto:atvs@uam.es)

## **DESCRIPTION OF DeepSignDB**

The DeepSignDB database comprises a total of 1526 users from four different popular databases and a novel signature database not presented yet, named e-BioSign DS2. Fig. 1 graphically summarises the design, acquisition devices, and writing tools considered in the DeepSignDB database.

![](http://atvs.ii.uam.es/atvs/DeepSignDB_Database.png)

Figure 1. Description of the design, acquisition devices, and writing tools considered in the new DeepSignDB database. A total of 1526 users and 8 different captured devices are used (5 Wacom and 3 Samsung general purpose devices). For the Samsung devices, signatures are also collected using the finger. Gen. Sig. = Genuine Signatures, and Sk. Forg. = Skilled Forgeries.

A short description of each database regarding the device, writing input, number of acquisition sessions and time gap between them, and type of impostors is included inside the paper [ICDAR2019_DeepSignDB].

## **STANDARD EXPERIMENTAL PROTOCOL**

The **DeepSignDB** database has been **divided into two different datasets,** one for the development and training of the system and the other one for the final evaluation. **The development dataset comprises around 70% of the users of each database whereas the remaining 30% are included in the evaluation dataset**. It is important to note that each dataset comprises different users in order to avoid biased results. Thus, we first identified all those users that took part in the acquisition of different databases.

For the training of the systems, the **development dataset** comprises a total of 1084 users. In our experiments carried out in [ICDAR2019\_DeepSignDB], we have divided this dataset into two different subsets, training (80%) and validation (20%). However, as this dataset is used only for development, and not for the final evaluation of the systems, **we prefer not to set any restriction and let researchers use it as they like.**

For the **final testing of the systems**, the remaining 442 users of the DeepSignDB database are included in the **evaluation dataset**. In order to **perform a complete and fair analysis of the signature verification systems**, and see their generalization capacity to different scenarios, aspects such as the inter-session variability, number of training signatures, impostor scenario, and writing input (stylus/finger) have been considered in the final experimental protocol design. 

**Table 1** describes all the experimental protocol details of the DeepSignDB **evaluation dataset** for both stylus (top) and finger (bottom) writing inputs.

![](http://atvs.ii.uam.es/atvs/DeepSignDB_Experimental_Protocol.png)

Table 1: Experimental protocol details of the DeepSignDB evaluation dataset (442 users). Numbers are per user and device.

For the moment, **we are able to release part of the evaluation dataset together with the corresponding signature comparisons files** considered during the evaluation of the systems in order to provide an easily reproducible framework. **We will contact all applicants as soon as possible in order to provide access to more dev/eval datasets as well**.

All data provided is organised as follows:

```shell
DeepSignDB
|-- Development
|-- Evaluation
    |-- Finger
    |-- Stylus
        
Comparison_Files
|-- Finger
    |-- 1vs1
        |-- Random
        |-- Skilled
    |-- 4vs1
        |-- Random
        |-- Skilled
|-- Stylus
    |-- 1vs1
        |-- Random
        |-- Skilled
    |-- 4vs1
        |-- Random
        |-- Skilled

```

We provide all details regarding comparison files and nomenclature in the “README.pdf” file send it when applying for the DeepSignDB database. 


## **REFERENCES**

For further information on the database and on different applications where it has been used, we refer the reader to (all these articles are publicly available in the [publications](http://atvs.ii.uam.es/atvs/listpublications.do) section of the BiDA group webpage.)

- [ICDAR2019_DeepSignDB] R. Tolosana, R. Vera-Rodriguez, J. Fierrez, A. Morales and J. Ortega-Garcia, "Do You Need More Data? The DeepSignDB On-Line Handwritten Signature Biometric Database", in Proc. Int. Conf. on Document Analysis and Recognition, ICDAR, Sydney, Australia, 2019.

- [PAA2010_BiosecurID] J. Fierrez, J. Galbally, et al., "BiosecurID: A Multimodal Biometric Database", Pattern Analysis and Applications, Vol. 13, n. 2, pp. 235-246, May 2010. 

- [VISP2003_MCYT] J. Ortega-Garcia, J. Fierrez, et al., "MCYT Baseline Corpus: A Bimodal Biometric Database", IEEE Proc. Vision, Image and Signal Processing, Vol. 150, n. 6, pp. 395-401, December 2003. 

Please remember to reference articles [ICDAR2019_DeepSignDB, PAA2010_BiosecurID, VISP2003_MCYT] on any work made public, whatever the form, based directly or indirectly on any part of the DeepSignDB database.
