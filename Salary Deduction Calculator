  // Function to calculate  tax based on the KRA rates
 function calculateTax( salary){
    let tax = 0;

    //KRA tax bands
    if (salary <= 34000) {
        tax = salary * 0.1; // 10% tax rate
    }
    else if (salary <= 45000){
        tax = (34000 * 0.1) + ((salary - 34000) *0.2); //20% tax rate
    }
    else if (salary <= 140000){
        tax = (34000 * 0.1) + (34000 * 0.2) + ((salary - 45000) * 0.25); //25% tax rate
    }
    else {
        tax = (34000 * 0.1) + (34000 * 0.2) + (74000 * 0.25) + ((salary - 140000) * 0.3); //30% tax rate
    }
    return tax;
 }

 //function to calculate NHIF deductions
   function calculateNHIF(salary){
    if (salary <= 6999) {
        return 150;
    }
    else if (salary <= 8999) {
        return 300;
    }
    else if(salary <= 12999) {
        return 400;
    }
    else if (salary <= 18999) {
        return 500;
    }
    else if (salary <= 24999) {
        return 600;
    }
    else if (salary <= 30999) {
        return 700;
    }
    else if (salary <= 35999) {
        return 800;
    }
    else if (salary <= 40999) {
        return 950;
    }
    else if (salary <= 45999) {
        return 1000;
    }
    else{
        return 1200;
    }
   }

   function calculateNSSF(basicSalary) {
    return basicSalary * 0.06; //Example of calculation
   }

   function getInputs() {
    const basicSalary = 2160; //Example of input
    const nssf = calculateNSSF(basicSalary);
    console.log('NSSF:', nssf);
   }

   //Finally call your getInputs to run your calculations
   getInputs();

   //function to calculate NSSF deductions
   async function getInputs() {
    const basicSalary = await parseFloat(4160);
    const benefits = await parseFloat(1280);
       console.log("Basic salary:" + basicSalary);
       console.log("Benefits:" + benefits);






  //gross salary
  const grossSalary = basicSalary + benefits;
  //the deductions
  const tax = calculateTax(basicSalary);
  const nhif = calculateNHIF(basicSalary);
  const nssf =calculateNSSF(basicSalary);
     //calculate the net salary finally
     const netSalary = grossSalary - tax - nhif - nssf;
     //the expected results
    console.log("Gross Salary:" + grossSalary);
    console.log("NHIF Deductions:" + nhif);
    console.log("NSSF Deductions:" + nssf);
    
   }
    //running the net salary calculator
     getInputs();