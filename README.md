# Home-Credit-Default-Risk
Kaggle Competition Dataset

This is my Analysis and Modelling for Kaggle Home Credit Dataset.

## EDA Home Credit

#### Dataset Shape : <br>
<img width="292" alt="image" src="https://user-images.githubusercontent.com/12759769/185772790-e4c009e2-f541-439c-bb93-9119f7f13776.png">

#### Train data Statistik : <br>
<img width="829" alt="image" src="https://user-images.githubusercontent.com/12759769/185774024-8195f149-4cce-4dac-8184-04b573c9eaa2.png">

#### Data distribution by label : <br>
<img width="569" alt="image" src="https://user-images.githubusercontent.com/12759769/185774052-5fecc962-7396-4e95-9d68-105b6dff76e8.png">

0 : All other cases <br>
1 : Client with late payment

Imbalanced Data distribution on label, so we can do Oversampling/Undersampling when create model. 

#### Some of categorical features plot : <br>
<img width="718" alt="image" src="https://user-images.githubusercontent.com/12759769/185776092-6e21bed9-7446-4b45-aee3-26e8619362bc.png">
<img width="707" alt="image" src="https://user-images.githubusercontent.com/12759769/185776113-163fd615-2634-4f34-8466-067098ac7516.png">
<img width="698" alt="image" src="https://user-images.githubusercontent.com/12759769/185776137-ad765c05-6959-405a-8a51-94c2c139b360.png">
<img width="719" alt="image" src="https://user-images.githubusercontent.com/12759769/185776149-55627859-22bc-4a08-b4fe-1600d5197d4b.png">

We got some rare values in categorical features, I got 3 ways to handle this type of data.
1. Binning rare category into new category.
2. Encode using TargetCategory method.
3. Encode using One-Hot Encoding method.

I'll choose the 3rd way to handle this rare values.

#### Missing Value

there are few missing value as XNA in CODE_GENDER feature. <br>
<img width="712" alt="image" src="https://user-images.githubusercontent.com/12759769/185776996-9aabc374-959b-4068-9f6b-d9aef2e30fa8.png">

a lot missing value in ORGANIZATION_TYPE. <br>
<img width="698" alt="image" src="https://user-images.githubusercontent.com/12759769/185777035-602fba8a-18b5-4c1d-9a99-ce0d95a6c04f.png">

I'm gonna drop observation with missing value in COODE_GENDER, and impute another missing value using KNNImputer <br>
