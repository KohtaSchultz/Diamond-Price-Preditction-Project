# Diamond-Price-Preditction-Project
I'm going to figure out what contributes to the price of a diamond.
Link to notebook at the bottom of the page.

# Hypothesis:
It's more than just the carats, cut, or color of a diamond that raises/ lowers the price of a diamond

# Step 1: Learn about diamonds:

This dataset only has data on "round brilliant diamonds" which account for 70% of the diamond market. These diamonds are used in things such as engagement rings.

   # Carat:

Carat is simply the weight of a  diamond. Below is a chart to help visualize the carat of a diamond.

![Visual representation of Carat](https://yourdiamondguru.com/wp-content/uploads/2018/01/Diamond-Carat-Chart-1.jpg)

This dataset goes from 0.2 carats for the min to 5.01 at the max. 

found on: [this site](https://yourdiamondguru.com/carat/)
"One carat is equivalent to around 200 milligrams (0.20 grams)."

   # Cut:

1. "Some professionals consider cut the most important C of diamond quality. "
I intend to find out whether this will turn out to be true, according to the data.

2. "The result was the GIA Cut Grading System, which evaluates the cut quality of a round brilliant diamond along a five-point scale ranging from Excellent to Poor.

A GIA cut grade evaluates:

    How the diamond appears when viewed face-up based on the attributes of brightness, fire and scintillation
    How well the diamond was designed to ensure durability and optimal weight
    The quality of the workmanship or craftsmanship that went into aligning and polishing the diamond’s facets"

![Diamond cut quality flowchart](https://4cs.gia.edu/wp-content/uploads/2018/04/690x460-damond-cut.jpg)

3: "A key component of a GIA diamond cut grade is the diamond’s face-up appearance – or how the diamond looks when viewed from above"

"When you see internal and external white light reflected from a diamond, you’re noticing “brightness.” If you see the scattering of light into all the colors of the rainbow,  you’re being treated to “fire.” Sparkle is actually “scintillation,” the pattern of bright and dark areas caused by reflections within the diamond as it or the light source moves."

4: "A diamond’s proportions can help predict how well a diamond will deliver brightness, fire and scintillation. However, an important outcome of GIA’s cut research was the finding that there is no single set of proportions that defines a well-cut round brilliant diamond. In fact, diamonds with different proportions can receive the same cut grade."

![Proportions Image](https://4cs.gia.edu/wp-content/uploads/2018/04/91622-690x460-diamond-cut-proportion-illustration.jpg)

5: "design and craftsmanship evaluate the quality of the diamond’s manufacture. Poor design could add unnecessary weight to a diamond or cause durability issues"
  "Design refers to decisions made during the fashioning process that determine the diamond’s physical shape, as seen in its proportions, weight ratio and durability."
  "Durability in the case of a round brilliant diamond refers to the risk of damage that might result from an extremely thin girdle."
  "Craftsmanship describes the care that went into fashioning the diamond, as seen in its polish and symmetry."

6: "GIA evaluates a round brilliant diamond’s cut based on seven components – brightness, fire, scintillation, weight ratio, durability, polish and symmetry – to arrive at a GIA diamond cut grade, which ranges from Excellent to Poor. The grade is set by the lowest assessment the diamond receives for five of the seven components."

![Cut Scale Image](https://4cs.gia.edu/wp-content/uploads/2018/04/162517-690x460-cut-scale.jpg)

[Source for this section](https://4cs.gia.edu/en-us/blog/gia-diamond-cut-grade-six-things-to-know/#how-GIA-assigns-diamond-cut-grade)

*The dataset goes from Fair, Good, Very Good, Premium, then Ideal, unlike the GIS scale.*

   # Color:

![This is the color scale](https://www.cleanorigin.com/blog/wp-content/uploads/2022/01/Diamond-Color.jpeg)

found on: [this site](https://www.cleanorigin.com/blog/diamond-color/)

The dataset only has colors from D - J; AKA colorless to near colorless. Although color can be scaled all the way down to 'Z', the person that compiled this dataset decided to only use diamonds that rank high on the color scale.

   # Clarity:

    "Flawless (FL) No inclusions and no blemishes visible under 10x magnification
    Internally Flawless (IF) No inclusions visible under 10x magnification
    Very, Very Slightly Included (VVS1 and VVS2) Inclusions so slight they are difficult for a skilled grader to see under 10x magnification
    Very Slightly Included (VS1 and VS2) Inclusions are observed with effort under 10x magnification, but can be characterized as minor
    Slightly Included (SI1 and SI2) Inclusions are noticeable under 10x magnification
    Included (I1, I2, and I3) Inclusions are obvious under 10x magnification which may affect transparency and brilliance"

[CLarity Source](https://4cs.gia.edu/en-us/diamond-clarity/)

The highest quality of diamond: "FL" isn't in the dataset, as well as "I2" and "I3", the lowest two levels of clarity.

![image](https://user-images.githubusercontent.com/114529109/214884594-ca20dbef-e78c-40f8-b1ba-99af1651125c.png)

   # Table and Depth
      *Ideal Percentages*
      Depth is how tall the diamond is from the flat table at the top to the point (aka culet) at the bottom, and depth *percentage* is:
      "Depth percentage is calculated by dividing the diamond’s total height by its total width. The deeper the diamond’s depth, the higher the diamond’s depth percentage."
    "For a round diamond, an ideal depth percentage is between 59 and 62.6 percent"
      Table is the flat surface at the face of the diamond. 100% is the diameter of the girdle.
    "For a round cut diamond, an excellent table range is 54 and 57 percent " 
    x is length, y is width, and z is depth. Z shouldn't be confused with depth because z is the total depth while depth is short for the depth percentage.
   
    
 [source](https://www.diamonds.pro/education/diamond-depth-and-table/)

# Step 2: narrow down dataset through querying:
I uploaded a [dataset](https://www.kaggle.com/datasets/swatikhedekar/price-prediction-of-diamond) from Kaggle into BigQuery to figure some things out about the data.
The descriptions for each column were lacking once uploaded, so I copy/pasted from the Kaggle page to the descriptions in BQ.
![image](https://user-images.githubusercontent.com/114529109/213885553-ca292309-64ce-4b18-a97d-3ce287c880e4.png)


Narrowed down to the best diamonds:

![image](https://user-images.githubusercontent.com/114529109/214903478-be2e404b-d625-4fea-8d0c-08b7c6a36d9e.png)



From ▲ to ▼


![image](https://user-images.githubusercontent.com/114529109/213885522-3677ca0e-cc7d-4297-b1d5-01157e3dcdaf.png)


# Conclusion
The carat of a diamond is the single most important factor in the price of a diamond. Color is the second most "important" farctor and is a far cry from actually driving the price compared to carat.
[Evidence](https://deepnote.com/workspace/uni-b780-ef93fdef-c706-47b3-b054-4b4a1e6442fe/project/Untitled-project-a8827c41-a145-4d77-8d43-44dc51b02862/notebook/Notebook%201-ba1dfcd423ac4559abb9ce51cf3a7b03)
