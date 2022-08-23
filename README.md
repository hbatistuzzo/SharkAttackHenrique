# SharkAttackHenrique
  Project status: completed (but more can be done regarding visualization)

# Project objective
  The goal of this project is to use a database of shark attacks to obtain information regarding the 3 species more likely to assault humans: White sharks, Tiger sharks and Bull sharks. Some of the attacks are fatal while others result in injuries only. By filtering the information therein, we can find the proportion of fatal attacks by species and answer a specific question: which species is more lethal?

# Methods
  - Cleaning
  - Filtering
  - Regex
  - Visualization

# Technologies 
  - Python
  - Pandas

# Project Description
  Dataset came from https://www.sharkattackfile.net/, whose goals are to "demonstrate and emphasize, through forensic analysis, the significance of shark/human interactions in comparison to the myriad dangers that we face in our daily lives". It logs all kinds of shark attacks registered since the 1820's, with specifics regarding activity, lethality, information of related parties and sources. The data therein is somewhat "dirty", meaning it has not been normalized by data analysis standards, hence providing a didactic opportunity for beginners in the field.

# Steps
  1) A preliminary inspection of the dataset reveals an extensive ammount of rows with no information (NaN's), which comprise pver 65% of the total rows. These rows can be eliminated with the pandas.DataFrame.dropna method to reduce the overall size of the dataset.
  2) Besides the rows, not all columns are useful for the purposes of this project. We can define a new dataset which imports only the 'Species' and 'Fatal y/n' columns from the original data.
  3) With this greatly reduced dataset, we can now find information for specific species. By using the pandas.DataArray.str.contains method, in tandem with regex, it is possible to filter the rows which contain, for example, the term 'White' or 'white'. In total, there are 667 entries regarding White sharks, 285 entries for Tiger sharks and 187 entries for Bull sharks.
  4) Inside these datasets filtered by species, we can use the pandas.DataArray.value_counts method on the 'fatal_(y/n)' column to find the proportion of lethal and non-lethal attacks.
  5) Finally, a simple division yields the percentage of lethal attacks. Respectively, for White, Bull and Tiger sharks, these are: 29.82%, 35.09% and 28.27. 

# Conclusion
  Hence, by inspecting this dataset, we find that attacks from the Bull shark species are more likely to result in a fatality. This result is corroborated by the following news articles from National Geographic (https://www.nationalgeographic.com/animals/fish/facts/bull-shark) and CBS (https://www.cbsnews.com/pictures/five-most-dangerous-sharks-to-humans/#:~:text=Bull%20Shark,lack%20of%20easily%20identifiable%20markings), which state that "Great Whites get most of the headlines but Bull Sharks may be the most dangerous shark of them all"!
  
# Contact
  https://www.linkedin.com/in/henrique-batistuzzo-2608b0136/
  https://github.com/hbatistuzzo
  https://www.youtube.com/channel/UCTihcuVi7oC3RgMPvS5l7Jw
  