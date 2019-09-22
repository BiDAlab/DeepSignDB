# DeepSignDB

## **INSTRUCTIONS FOR DOWNLOADING DeepSignDB**

1. [Download license agreement](http://atvs.ii.uam.es/atvs/licenses/e-BioDigit_License.pdf), send by email one signed and scanned copy to [**atvs@uam.es**](mailto:atvs@uam.es) according to the instructions given in point 2.
2. Send an email to [**atvs@uam.es**](mailto:atvs@uam.es), as follows:

    _Subject:_ **[DATABASE download: DeepSignDB]**

    Body: Your name, e-mail, telephone number, organization, postal mail, purpose for which you will use the database, time and date at which you sent the email with the signed license agreement.

1. Once the email copy of the license agreement has been received at ATVS, you will receive an email with a username, a password, and a time slot to download the database.
2. [Download the database](http://atvs.ii.uam.es/atvs/intranet/free_DB/e-BioDigit), for which you will need to provide the authentication information given in step 4. After you finish the download, please notify by email to [**atvs@uam.es**](mailto:atvs@uam.es) that you have successfully completed the transaction.
3. For more information, please contact: [**atvs@uam.es**](mailto:atvs@uam.es)

## **DESCRIPTION OF DeepSignDB**

The DeepSignDB database comprises a total of 1526 users from four different popular databases (i.e., MCYT, BiosecurID, Biosecure DS2, and e-BioSign DS1) and a novel signature database not presented yet, named e-BioSign DS2. Fig. 1 graphically summarises the design, acquisition devices, and writing tools considered in the DeepSignDB database.



Figure 1. Description of the design, acquisition devices, and writing tools considered in the new DeepSignDB database. A total of 1526 users and 8 different captured devices are used (5 Wacom and 3 Samsung general purpose devices). For the Samsung devices, signatures are also collected using the finger. Gen. Sig. = Genuine Signatures, and Sk. Forg. = Skilled Forgeries.

A short description of each database regarding the device, writing input, number of acquisition sessions and time gap between them, and type of impostors is included inside the paper [ICDAR2019\_DeepSignDB].

## **STANDARD EXPERIMENTAL PROTOCOL**

The **DeepSignDB** database has been **divided into two different datasets,** one for the development and training of the system and the other one for the final evaluation. **The**** development dataset comprises around 70% of the users of each database ****whereas the**** remaining 30% are included in the evaluation dataset**. It is important to note that each dataset comprises different users in order to avoid biased results. Thus, we first identified all those users that took part in the acquisition of different databases. Additionally, we corrected several mistakes we found along the different databases.

For the training of the systems, the **development dataset** comprises a total of 1084 users. In our experiments carried out in [ICDAR2019\_DeepSignDB], we have divided this dataset into two different subsets, training (80%) and validation (20%). However, as this dataset is used only for development, and not for the final evaluation of the systems, **we prefer not to set any restriction and let researchers use it as they like.**

For the **final testing of the systems** , the remaining 442 users of the DeepSignDB database are included in the **evaluation dataset**. In order to **perform a**** complete and fair analysis of the signature verification systems**, and see their generalization capacity to different scenarios, aspects such as the inter-session variability, number of training signatures, impostor scenario, and writing input (stylus/finger) have been considered in the final experimental protocol design.

**Table 1** describes all the experimental protocol details of the DeepSignDB **evaluation dataset** for both stylus (top) and finger (bottom) writing inputs.

#### Table 1: Experimental protocol details of the DeepSignDB evaluation dataset (442 users). Numbers are per user and device.

For the moment, **we release the evaluation dataset** composed of 442 users **together with the corresponding signature comparisons files** considered during the evaluation of the systems in order to provide an easily reproducible framework:

STYLUS SCENARIO

- Skilled Forgeries: &quot;Comp\_skilled\_stylus.txt&quot;
- Random Forgeries: &quot;Comp\_random\_stylus.txt&quot;

FINGER SCENARIO

- Skilled Forgeries: &quot;Comp\_skilled\_finger.txt&quot;
- Random Forgeries: &quot;Comp\_random\_finger.txt&quot;

Genuine comparisons are set to &quot;0&quot; whereas impostor comparisons are set to &quot;1&quot;. In order to run the evaluation easily, we recommend unfolding all signatures of the database in the same folder of the comparison files. It is important to highlight that **these comparison files provide all comparisons carried out for the scenario of having just one training signature (1vs1 case)**.

For the scenario of using 4 training signatures (4vs1 case), researchers can perform the average score of the 4 one-to-one comparisons (as we did) or build user models using the 4 training signatures described in the comparisons files (e.g., through HMM models).

**Finally, we also plan to release the development dataset (1084 users) as soon as possible.**

#### **DATABASE FORMAT**

Each user of the database has its corresponding folder. The nomenclature followed to name each folder is: uA\_B\_C\_D

-  A: indicates the number ID of the user.
-  B: indicates whether it is the development [d] or the evaluation [e] dataset.
-  C: indicates the name of the database where the user comes from [MCYT, BiosecurID, BioSecure\_DS2, e\_bioSign\_DS1, e\_bioSign\_DS2].
-  D: indicates the number ID of the user in the original database.

#### **SIGNATURE FILES FORMAT**

Each handwritten signature is stored in a different text file. Genuine signatures are indicated as &quot;\_g\_&quot; whereas skilled forgeries as &quot;\_s\_&quot;. Regarding the content of each file, we have decided to keep the same format as in the original databases to avoid confusion. All signatures follow the same format:

- ROW 1: it just contains one entry with the number of sampled points of the handwritten signature (N).
- ROWS 2 to (N+1):
  - COLUMN 1: represents the X coordinate.
  - COLUMN 2: represents the Y coordinate.
  - COLUMN 3: represents the timestamp.

However, pressure information (not available when using the finger) is stored in different columns depending on the database:

-
  - MCYT: column 6.
  - BiosecurID and Biosecure\_DS2: column 7.
  - e\_bioSign\_DS1 and e\_bioSign\_DS2: column 4.

The remaining of the columns not described here can provide other information acquired by the sensor (e.g., azimuth and altitude angles).

#### **REFERENCES**

For further information on the database and on different applications where it has been used, we refer the reader to (all these articles are publicly available in the [publications](http://atvs.ii.uam.es/atvs/listpublications.do) section of the BiDA group webpage.)

- [ICDAR2019\_DeepSignDB] R. Tolosana, R. Vera-Rodriguez, J. Fierrez, A. Morales and J. Ortega-Garcia, &quot;Do You Need More Data? The DeepSignDB On-Line Handwritten Signature Biometric Database&quot;, in Proc. Int. Conf. on Document Analysis and Recognition, ICDAR, Sydney, Australia, 2019.

Please remember to reference articles [ICDAR2019\_DeepSignDB] on any work made public, whatever the form, based directly or indirectly on any part of the DeepSignDB database.
