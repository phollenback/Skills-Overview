Abstraction is easily explainable, and hard to implement. An easy way to explain to a beginner how abstraction is implemented is to show them an complex application's main method. For example this main method is implemented in a mock console store.
```
    boolean live = true;
		// While store is still 'active'
		while(live)
		{
			// check input and proceed process
			switch(input)
			{
				// view inventory
				case 1: 
					// print inventory
					store.printList(store.inv.getInventory());
					// Prompt next steps
					store.printMenu();
					// gather Input
					input = scnr.nextInt();
					break;
				// Make a purchase
				case 2:
					// start purchase process
					store.purchaseItem();
					// prompt next step
					store.printMenu();
					// gather next menu option
					input = scnr.nextInt();
					break;
				// cancel purchase
				case 3: 
					// begin cancel process
					store.cancelPurchase();
					// prompt next step
					store.printMenu();
					// gather next menu option
					input = scnr.nextInt();
					break;
			    // view cart
				case 4:
					// print cart
					store.printList(store.cart.returnCart());
					// prompt next step
					store.printMenu();
					// gather next menu option
					input = scnr.nextInt();
					break;
				// clear cart
				case 5:
					// clear cart
					store.cart.clearCart();
					// print list to check if null
					store.printList(store.cart.returnCart());
					// print menu
					store.printMenu();
					// gather next menu option
					input = scnr.nextInt();
					break;
				// leave store
				case 6:
					try 
					{
						// save back to file
						store.inv.saveInventory();
					} 
					catch (DataHandlingException e)
					{
						System.out.println(e.getMessage());
					}
					catch(InventoryErrorException e)
					{
						System.out.println(e.getMessage());
					}
					// breaks store
					live = false;
					break;
			}
		}
		// Prompt goodbye statement
		System.out.println("Thanks for stopping by. Have a nice day.");
		
		
	}

```
