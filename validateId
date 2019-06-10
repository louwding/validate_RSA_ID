class validateID {
  // Validate a RSA ID Number
  public static validateIdNo(idNo: string): boolean {
    // Length must be 13
    if (idNo.length == 13) { 
      //let evenString: string = '';
      let evenConcat: string = '';
      let oddSum: number = 0;
      let evenSum: number = 0;

      // Add numbers in odd positions, excluding last digit
      // Concatinate numbers in even positions
      for (let i = 0; i < idNo.length - 1; i++) {
        //Add all of the digits in odd positions
        if ((i + 1) % 2 != 0) {
          oddSum += parseInt(idNo[i]);
        } else {
          evenConcat += idNo[i];
        }
      }

      // Multiply the concatinated even numbers by 2
      evenConcat = (parseInt(evenConcat) * 2).toString();

      // Add the concatinated numbers together
      for (let i = 0; i < evenConcat.length; i++) {
        evenSum += parseInt(evenConcat[i]);
      }

      // Add the sum of the odd and even positioned numbers together
      // Take the last digit and subtract it from 10
      // Take the last digit.
      let result: string = ((10 - ((oddSum + evenSum) % 10)) % 10).toString();

      // Check if the result digit is equal to the last digit of the ID number
      if (result == idNo[idNo.length - 1]) {
        return true;
      } else {
        return false;
      }
    } else {
      return false;
    }
  }  
}
