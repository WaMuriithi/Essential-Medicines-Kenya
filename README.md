# Essential-Medicines-Kenya
Investigating essential medicines that are not manufactured locally

<h1>Candidate Products for local Phamaceutical Manufacturing</h1> 

<p> 
  One point of convergence between the two leading coalitions in the 2022 election was the need to increase local manufacturing of medicines and medical devices. This resolve can only have been strengthened with the recent rapprochement of the groups and the still acute need to roll out universal health coverage, the sustainability of which rests on managing healthcare costs, with 20-60% of healthcare costs in developing countries attributed to medicines (Cameron et al., 2009). Increasing self-sufficiency in pharmaceuticals and medical devices offers other advantages, including creating quality jobs, import substitution, export promotion, and health security, particularly with the lessons of the COVID-19 pandemic when source markets blocked the export of essential drugs and active pharmaceutical ingredients, such as paracetamol. 
</p>
<p>
  While the government has a raft of incentives for local and foreign investors to set up in Kenya, uptake has been slow, chiefly blamed on ineffective policy and regulatory environments, skills gaps in research and development, and operational challenges in electricity and water supply (International Finance Corporation, 2020). An overlooked driver is the lack of quality data on medicines, devices, and commodity needs, an anachronistic situation judging from the considerable investments in computerizations of processes at the Pharmacy and Poisons Board (PPB), Kenya Trade Network Agency, and other public and private players in trade and healthcare. I report on exploratory analysis of publicly available data to advise on immediate-release oral dosage forms that new or established investors can consider manufacturing locally. 
</p>
<h3>
  Datasets and Data Cleaning
</h2>
<p> 
  I extracted the list of registered products from the PPB website using Selenium and Python and the essential medicines list from the Kenya Essential Medicines List 2023 (KEML) using Power Query. The Python code and extracted datasets are available on my GitHub page. The PPB registered products list contains 12 fields (registration number, international non-proprietary name, and local/foreign key fields). The dataset lacks an apparent format, especially in the INN column, thus requiring Pandas and strenuous Excel hand cleaning. At the same time, the list includes veterinary and human products. The KEML lists are well formatted with five fields (name of medicine, dose-form, and strength/size key fields); most of the cleaning could be done in Pandas, but limited hand cleaning in Excel is necessary to convert common drug names to recommended International Non-proprietary Names (INN). Other data cleaning activities included renaming and deleting columns not required in the analysis, removing duplicates, standardizing INNs, filling null values, and splitting footnote references from product names. 
</p>
<h3>
  Analysis and Insights
</h3>
<p>
  The cleaned datasets containing single INNs or fixed-dose preparations were compared to extract essential medicines not manufactured locally. A comparison of the recommended formulations and strengths available from local manufacturers was not performed due to data quality challenges in the PPB list, as indicated previously. The analysis identified 417 essential medicines that are not manufactured locally. Prominent in the list are anticancer drugs, injectable antibiotics, and general and local anesthetics. While this is not surprising due to skills gaps, limited access to long-term financing, and deficiencies in regulatory capacity, several products marketed as immediate-release solid oral formulations and eligible for biowaivers using the bio-pharmaceutical classification system (BCS) were noted (see Table 1). 
</p>
<p>
  The analysis yielded 28 BCS class I, 12 BCS class III, and six fixed-dose combinations of either class I and III or class III marketed as immediate-release solid oral formulations (excluding antineoplastics) that manufacturers can target due to their relative ease of development and registration. PPB has adopted international guidelines for registration of multisource (generic) products that permit registration of class I products as therapeutic equivalents of innovator or reference-listed drugs based on acceptable in vitro bioavailability tests. Class III products (high solubility, low permeability) are also eligible for waivers of in vivo bioavailability and bioequivalence tests provided the sponsor demonstrates very rapid dissolution of the API in the generic and reference (≥ 85% of labeled amount dissolves in ≤ 15 minutes) and that the excipients in the generic product are qualitatively the same and quantitively similar to the reference.
</p>
<h3>
  Conclusion
</h3>
<p>
  Manufacturing pharmaceuticals and medical commodities in Kenya remains an untapped opportunity for local and foreign investors. Apart from the increasing demand for medical services—pushed by a growing population, expanding middle class, and public policy towards universal access, Kenya is well placed to serve as a manufacturing hub for the 1 billion plus Sub-Saharan African population. This review uncovered over 40 drugs Kenya-based manufacturers may target for import substitution. Discerning investors should triangulate the information with market size figures.
</p>

<table>
<caption> Table 1: Selected INNs Eligible for Biowaver </caption>
<tr>
  <th>Formulation</th>
  <th>BCS Class I</th>
  <th>BCS Class III*</th>
</tr>
<tr>
  <td>Immediate release solid containing one API/INN</td>
  <td>ketorolac, labetalol, metoprolol, moxifloxacin, dihydrocodeine, letrozole, trimetazidine, verapamil, levofloxacin, tranexamic acid, warfarin, donepezil</td>
  <td>clindamycin, lenalidomide, pantoprazole, pyridostigmine, tenofovir alafenamide, misoprostol, linagliptin, pyridostigmine</td>
</tr>
<tr>
  <td>Immediate-release solid fixed dose combination</td>
  <td></td>
  <td>artesunate + pyronaridine, levodopa + carbidopa, perindopril + amlodipine, empagliflozin + metformin, mifepristone + misoprostol, sitagliptin + metformin</td>
</tr>
  
</table>
<p><em>Note:</em> *Only very rapidly dissolving BCS Class III products are eligible for biowaiver. The intrinsic solubility of BCS III INNs was not checked.</p>
