Here I used Google Colab to use a GPU for training   

Data was obtained from http://www.trumptwitterarchive.com/archive  
<br>

<b><i>Different ways to upload dataset to colab:</i></b>      
- From Github : Click on the dataset in your repository, then click on View Raw. Copy the link to the raw dataset and store it as a string variable called url in Colab. Then do pd.read_csv(url) to read the file.      
- From a local drive :   
<b>from google.colab import files  
uploaded = files.upload()</b>     
It will prompt you to select a file. Click on “Choose Files” then select and upload the file. Wait for the file to be 100% uploaded. You should see the name of the file once Colab has uploaded it. Then type in the following code to import it into a dataframe (make sure the filename matches the name of the uploaded file).  
<b>import io   
df2 = pd.read_csv(io.BytesIO(uploaded['Filename.csv']))</b>  

Dataset is now stored in a Pandas Dataframe    

Ref Link : https://towardsdatascience.com/3-ways-to-load-csv-files-into-colab-7c14fcbdcb92
