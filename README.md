# Practice_Ultra
 //1. Temperature Advisor
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the temperature: ");
        double temp = sc.nextDouble();

        if (temp <0){
            System.out.print("Wear a heavy coat");
        } else if (temp <=15) {
            System.out.print("Wear a jacket");
    } else if (temp <=25){
                System.out.print("Light clothing");
} else if(temp >25){
        System.out.print("Very hot");

        //2. Username Validator
        System.out.print("Enter a username: ");
            String regex = "^[A-Za-z][A-Za-z0-9]{4,11}$";
            String username = sc.nextLine();

            if (username.matches (regex)) {
                System.out.println("Valid username");
            } else {
                System.out.println("Invalid username");
                

        // 3. Parking Fee Calculator
        System.out.print("Enter number of hours: ");
            double hours = sc.nextDouble();
            double rebate;

            if (hours <= 2) {
                rebate = hours * 5;

            } else if (hours <= 5) {
                rebate = 10 + (hours - 2) * 4;

            } else {
                rebate = 10 + 12 + (hours - 5) * 3;

            }
            if (rebate > 30) {
                rebate = 30;
            }
            System.out.print("Parking Fee: $" + rebate);

       

        //4. Online Order Discount System
        System.out.print("Enter purchase amount: ");
        double amount = sc.nextDouble();
        System.out.print("Enter membership type (G/S/N): ");
        char membership = sc.next().toUpperCase().charAt(0);
        double finalPrice;

        switch (membership) {
            case 'G' :
                if (amount >= 100) {
                    finalPrice = amount - (amount * 0.20);
                    System.out.println("Final price: " + finalPrice);
                } else {
            System.out.println("No rebate");
                }
                break;

            case 'S' :
                if (amount >= 100) {
                    finalPrice = amount - (amount * 0.10);
                    System.out.println("Final price: " + finalPrice);
                } else {
                    System.out.println("No rebate");
                }
                break;

                case 'N':
                if (amount >= 100) {
                    finalPrice = amount - (amount * 0.05);
                    System.out.println("Final price: " + finalPrice);
                } else {
                    System.out.println("No rebate");
                }
                break;

            default:
                System.out.println("Invalid membership type");
        //}

         // 5. Phone Number Formatter
        System.out.print("Enter phone number: ");
        String phone = sc.nextLine();

        String clean = phone.replaceAll("[\\s-]", "");
        System.out.println("After cleaning: " + clean);
        String regex = "^[0-9]{10}$";

        if (clean.matches (regex)) {
            System.out.println("Valid phone number");
        } else {
            System.out.println("Invalid phone number");
        }

        sc.close();
                }
