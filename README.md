# Currency_convertor

Dict = { 'USD' : 74.28, "Euro": 88.26}
INR = {"Euro": 88.26, "€": 88.26, "USD": 74.28,"$": 74.28}
EU_US= {"Eu": 1.19, "Us": 0.84}

amt= float(input("Enter amount you want to convert:"))

og_currency= (input("Enter currency (USD or Euro or INR):"))


# if its US foreign 

if og_currency == 'USD':
    currency_input = input("Enter desired currency in case-sensitive format (INR or Euro):")
    print(currency_input)
    
    if currency_input== 'Euro':
        print("€" + str(EU_US["Us"] * amt))
    
    elif currency_input== 'INR':
        print("Rs." + str(INR["USD"] * amt))
        
# if its EU foregin
        
    
elif og_currency == 'Euro':
    currency_input = input("Enter desired currency in case-sensitive format (INR or USD):")
    print(currency_input)
    
    if currency_input=='USD':
        print("$"+str(EU_US["Eu"] * amt))
    
    elif currency_input == "INR":
        print("Rs." + str(INR["Euro"] * amt))
            
# if its IN domestic

elif og_currency== "INR":
    currency_input = input("Enter desired currency in case-sensitive format (Euro or USD):")
    print(currency_input)
    
    if currency_input=="USD":
        print("$" + str(amt/Dict["USD"]))
              
    elif currency_input== "Euro":
        print("€" + str(amt/Dict["Euro"]))
