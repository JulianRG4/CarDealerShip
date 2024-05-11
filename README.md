# CarDealerShip
This is a Car DealerShip that allowes you to add, remove, and search by various options. 
the main class runs the application and starts the userInterface class. 
This class is stuctured as following and uses a switch stament in order to run until the user enters 99; it will then save changes made to the inventory Array lisyt and save them to the "Files/inventory.csv"
 public void run()
   {
      Scanner scanner = new Scanner(System.in);
      int choice = 0;
      while (choice != 99)
      {
         System.out.println();
         System.out.println("[1] - Find vehicles within a price range");
         System.out.println("[2] - Find vehicles by make / model");
         System.out.println("[3] - Find vehicles by year range");
         System.out.println("[4] - Find vehicles by color");
         System.out.println("[5] - Find vehicles by mileage range");
         System.out.println("[6] - Find vehicles by type (car, truck, SUV, van)");
         System.out.println("[7] - List ALL vehicles");
         System.out.println("[8] - Add a vehicle");
         System.out.println("[9] - Remove a vehicle");
         System.out.println("[99] - Quit");
         System.out.print("Enter your choice: ");
         choice = scanner.nextInt();

         switch (choice)
         {
            case 1:
               findVehiclesWithinPriceRange();
               break;
            case 2:
               findVehiclesByMakeModel();
               break;
            case 3:
               findVehiclesByYearRange();
               break;
            case 4:
               findVehiclesByColor();
               break;
            case 5:
               findVehiclesByMileageRange();
               break;
            case 6:
               findVehiclesByType();
               break;
            case 7:
               listAllVehicles();
               break;
            case 8:
               addVehicle();
               break;
            case 9:
               removeVehicle();
               break;
            case 99:
               DealershipFileManager.saveDealership(dealerShip);
               System.out.println("Exiting...");
               break;
            default:
               System.out.println("Invalid choice. Please try again.");
         }
      }
      scanner.close();
      All these methods simply call the ArrayList made in the dealership after the DealerShipFileManager creates the initial AarrayList which the other methods call from. 
      The DealerShipFileManager reads the first line of the file and then creates a second section for the following lines wich would consit of the vehiclew info. 
      We also have a vehicle class which is used to hold the vehicle variables and make our contructor for the restopf the workshop.
      I also incuded a few test that see if the add vehicle, remove vehicle, and search by color are working correctly.