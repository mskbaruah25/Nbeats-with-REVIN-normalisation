# Nbeats-with-REVIN-normalisation
To use nbeats with revin normalisation download the files nbeats_revin.py and nbeats_preprocessing.py. 
With whatever data you want to use make sure to bring it into the following format:
            Values  , Timestamps
            -----   ,   -----
            -----   ,   -----
            -----   ,   -----
            
Import the file nbeats_preprocessing.py and use the function 'make_windows' to get windows and labels. For example:  windows, labels = nbeats_preprocessing.make_windows(values, window_size = 7, horizon = 3)
After that input the windows and labels into the function train_test_split from the same file to get X_train, x_test, y_train, y_test. For example: X_train, x_test, y_train, y_test = train_test_split(windows, values)

Import nbeats_revin.py and use 'get_nbeats_revin_model' function to get the nbeats model with revin normalisation. Compile the model and fit to the data with proper callbacks to get the results.
            
       
