# FinTech Finder (Blockchain Payment System) - UW FinTech BootCamp Module 19 Challenge

This project is my blockchain payment app that uses [Ganache](https://trufflesuite.com/ganache/) and [Web3.py](https://web3py.readthedocs.io/en/v5/) to integrate Ethereum transactions to hire FinTech professionals.

The web UI is created using [Streamlit](https://streamlit.io/)

---

## Summary

Using Ganache, I create a personal Ethereum blockchain that the code connects to using Web3.py. With the Ethereum blockchain, transactions between the provided sample wallet addresses can be performed through the streamlit UI. 

![Screenshot of app main screen showing side bar that allows user to hire fintech professionals and pay them per hour using the mock ganache ethereum blockchain](./Resources/Images/app_main_screen.png)

Transactions are sent by selecting one of the FinTech professionals and defining an amount of hours you would like to hire them for. The app then outputs the hourly rate, Ethereum address, and the total wage in Ether depeding on your specified input. Using the "Send Transaction" button will then initiate a blockchain transaction by creating a block and distributing the required Ether from the Ganache wallet. 

![Gif showing the user specifying a fintech professional, setting a small number of hours, and using the send transaction button to initiate the blockchain transaction](./Resources/Gifs/send_transaction.gif)

In the Ganache UI you will be able to see that your wallet has reflected the transaction by decreasing the amount of Ether in your account balance. 

![Screenshot of Ganache UI showing the first wallet having a reduced (less than 100) wallet balance after making several transactions through the app](./Resources/Images/account_balance.png)

You can then verify further that the transactions were sent to the correct addresses by comparing the defined sample FinTech professional account numbers to the ones in each transaction listed in the Ganache transaction history. 

![Hard coded list of FinTech professionals and the sample account addresses](./Resources/Images/candidates.png)
![Screenshot of Ganache transaction between ganache wallet and sample FinTech professional](./Resources/Images/transaction_example.png)

The Ganache transaction history will also show all of the transactions made using the app. 

![List of transactions in the Ganache UI](./Resources/Images/transaction_history.png)

As you add transactions you will also be able to see them instantly reflected in the Ganache transaction history. 

![Gif showing a new transaction appear in the Ganache transaction history after being sent using the UI](./Resources/Gifs/new_transaction.gif)

---

## Technologies

This is a Python 3.7 project ran using the following dependencies:
1. [Pandas](https://github.com/pandas-dev/pandas) (1.3.5) - DataFrame objects
2. [Streamlit](https://streamlit.io/) (1.18.1) - Web interface

---

## Installation Guide

This project was ran using an [Anaconda](https://docs.anaconda.com/) dev environment but assuming you have Python installed you will likely also be able to run this app after installing the required dependencies with Pip: 

```Python
pip install pandas
pip install streamlit
```

The [requirements.txt](./Resources/requirements.txt) file in the Resources folder has the exact anaconda environment that I used in creating this project if you would like to copy it. 

Create a copy of the conda dev environment with `conda create --name myenv --file requirements.txt`

Then install the requirements with `conda install --name myenv --file requirements.txt`

---

## Usage

To run this app locally simply open a terminal window with this project as the main directory and type `streamlit run fintech_finder.py`. This will open the Streamlit web UI in your browser on localhost 8501. 

Caching is used to save any blockchain data that you use while running the app, however this data is lost after the session is over. 

---

## Contributors

[Ethan Silvas](https://github.com/ethansilvas)

---

## License

This project uses the [GNU General Public License](https://choosealicense.com/licenses/gpl-3.0/)