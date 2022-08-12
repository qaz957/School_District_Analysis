# School District Analysis

## Overview
The purpose of this analysis is to provide data on key metrics on the schools within a district without including the grades for Thomas High School's 9th grade class. There have been reports of academic dishonesty and we want to perform our inital analysis again without these values.

## Analysis
Using the [loc] method in Pandas, we can replace the values of the 9th grade classes math and readings scores with non-values, allowing us to re-do out analysis without them.

      student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), "math_score"] = np.nan
      
Our findings reveal that without the values from the 9th grade, the passing percentage of the scholl drops drastically.

![Thomas_Pass_Original](https://user-images.githubusercontent.com/108296899/184219522-3703ad04-b25a-4ff5-8f92-de2eb7542777.png)

Our intial analysis of the schools districsts found that Thomas High School ranked near the top of the district when it came to passing percentage. After removing that data, a new story is told.

![Thomas_Pass_Adjusted](https://user-images.githubusercontent.com/108296899/184219817-4a91f4db-c548-44ab-9e67-a466febe72cc.png)

Thomas High School more than likely ranks in the middle of the pack when is comes to academic performance.

### How does this data affect other metrics?
#### Grade
Predictably, removing the scores from one grade will not affect the others. This data remains unchanged.

#### Schools Spending
Spending $638/student Thomas High School falls with the spedning bin for $630-$644. Originally, that bin had a passing rate of 63%.

![School_Spending_Summary_Original](https://user-images.githubusercontent.com/108296899/184221661-5bae2d76-5e34-4743-84f4-77a61d06c09f.png)

After adjusting the data, we see that drop to 56%.

![School_Spending_Summary_Adjusted](https://user-images.githubusercontent.com/108296899/184221848-da9ab1e3-0f0c-4cab-a94f-6a383a53f1b5.png)

#### School Size

Thomas falls into the "Medium" school category. Similarly, we can see a 6 point drop in passing percentage for "Medium" schools

- Original:

![School_Size_Summary_Original](https://user-images.githubusercontent.com/108296899/184222301-d14987ac-b2cd-44e8-94e6-a671cb6eea99.png)

- Adjusted:

![School_Size_Summary_New](https://user-images.githubusercontent.com/108296899/184222312-9c860225-5531-4cd4-9ed0-f9a57b0d223a.png)

#### School Type

As a charter school Thomas affects the academic performance of other charter schools, decreasing by 3%.

- Original:
 
![School_Type_Summary_Original](https://user-images.githubusercontent.com/108296899/184222816-df6f3a47-8f8e-4a43-80aa-318a2482f1cd.png)


- Adjusted:
 
![School_Type_Summary_New](https://user-images.githubusercontent.com/108296899/184222868-6e352d61-dcdd-4908-b9b5-f64f132837b1.png)

## Summary

We can see here that these four metrics, although to different degress, have been affected by this academic dishonesty. Throwing this data can affect things like funding allocation and teacher performance. Even such a small sample size of discrepancy of data has a cascading effect on the rest of the demographics that Thomas High School falls within.
