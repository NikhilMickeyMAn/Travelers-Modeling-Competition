# Travelers-Modeling-Competition

![image](https://user-images.githubusercontent.com/120340630/211175909-00198d3a-b4e9-4efa-a8e4-5ca142f5a7dc.png)

## Project Description
You work for Peace of Mind Insurance Company in their personal automotive insurance department as a modeler. For personal auto, anyone that asks for an estimated price for a policy from your company (also known as a quote) will receive one. However, of those quoted, only a fraction will choose your company as their insurer (versus other companies they also received quotes from). Your team has been asked to build what’s known as a conversion model, with the goal of understanding the population of policies Peace of Mind Insurance Company is most likely to write (a.k.a. issue or convert). In other words, what types of customers is your company writing over its competitors?

### Your goals in this competition are as follows:
* Identify quoted policies that your company will convert (a.k.a. issue)
* Understand key characteristics of policies your company tends to write, as well as those they tend not to write (e.g. understand quoted policies with both high and low conversion rates)
* Provide a recommendation on how this information could be leveraged at Peace of Mind Insurance

## Data Description
The data provided to you and your team consists of variables describing customers that asked for quotes. There are three datasets: at the policy, driver, and vehicle levels. Each row of the policy dataset corresponds to a single policy, which may be associated with multiple drivers and vehicles. Likewise, each row of the driver dataset represents a single driver, and each row of the vehicle dataset represents a single vehicle. It's easy to check that each driver and each vehicle are associated with just one policy. You may assume that all members on a policy live at the same address.

Your company was only able to convert a fraction of the policies found in this sample. The policy dataset also has a training and test split variable called split. Note that the conversion indicator (the response variable) is missing for policies in the test split. Your task is to build a model on the training data and apply your model to predict the conversion indicator for each policy in test data.

### Policies.csv

policy_id: Unique customer identifier

Quote_dt: Date the quote was submitted

quoted_amt: Quote amount (US dollars)

Prior_carrier_grp: Prior carrier group

Cov_package_type: Level of coverage needed

discount: Whether or not a discount was applied to the quote amount

number_drivers: Number of drivers

credit_score: Credit score of primary policy holder

num_loaned_veh: Number of vehicles on policy that have a loan associated with them

num_owned_veh: Number of owned vehicles on the policy

num_leased_veh: Number of leased vehicles on the policy

total_number_veh: Total number vehicles on the policy

primary_parking: Where car(s) are primarily parked

CAT_zone: Catastrophe risk zone

Home_policy_ind: Does customer has existing home insurance policy with Peace of Mind

zip: US zip code of policy holder

state_id: State of policy holder

county_name: County of policy holder

Agent_cd: Unique agent code (8 digits)

split: Train/Test split

convert_ind: Conversion indicator (0=no, 1=yes). This is the response variable

### Drivers.csv:

policy_id: Unique customer identifier

gender: Gender of driver

age: Age of driver

high_education_ind: Higher education indicator

safty_rating: Safety rating index of driver

living_status: Driver’s living status (levels = ‘own’, ‘rent’, ‘neither’)

### Vehicles.csv:

policy_id: Unique customer identifier

car_no: Unique car identifier (per policy)

ownership_type: Whether the car is loaned, owned or leased

color: Vehicle color

age: Vehicle age

make_model: Make and model of the vehicle

NOTE
Training and Test sets are combined across the files, and need to be separated manually by your group!
