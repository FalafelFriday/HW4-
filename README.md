# HW4-
pandas hw


Prerequisites: Jupiter notebooks (or similiar program),pandas library,numpy library

Installations: use pip install to get pandas and numpy

Coding step 1: the first step is to import our dependencies (pandas and numpy), read in our csv file,and remove any NAs. after that I completed the first 
task which was to get the total amount of players it was pretty simple as iu just used the len function.

Coding step 2: In step 2 I completed the purchase analysis section and then created a new dataframe with the required variables. I trested 
by printing all the variables as i did each of them so that i know i got the right value 
SAMPLE
-----------------
average=df['Price'].mean()
#print(average)
Total_revenue=df['Price'].sum()
#print(Total_revenue)
total_purchases=len(df['Purchase ID'])
#print(total_purchases)
------------------


Coding step 3: In step 3 I worked on the gender analysis section, I used the nunique function to gather the amount of Males,Females,and Others
the main change was that i had to find the percentages of people who played the game by gender. N.B. an explination of the variables might be needed
Here is the key: dfmc,dffc,and dfoc are the number of players for that specific gender. dmpc,dfpc,dopc is the percent of the players by gender.
dfc is the total number of players.

SAMPLE
----------
dfmc = df[df["Gender"] == "Male"]["SN"].nunique()
dffc = df[df["Gender"] == "Female"]["SN"].nunique()
dfoc = dfc - dfmc - dffc
dmpc = ((dfmc/dfc)*100)
dfpc = ((dffc/dfc)*100)
dopc = ((dfoc/dfc)*100)
----------

Coding step 4: Now we move on to the ages. The first thing i did was print out the min and max ages of the players in the data, this allowed me to more accurately set my bins and labels and after that i grouped them and created the dataframe 

SAMPLE
------
agedmf=pd.DataFrame({"Total Counts":counts,"Percentage of Players":percent})
agedmf["Percentage of Players"]=agedmf["Percentage of Players"].map("{:.2f}%".format)
agedmf
-----

Coding step 5 and 6: these steps are fused as they are basically the same thing as all of the other ones
