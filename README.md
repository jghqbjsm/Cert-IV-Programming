package footballoutput;

/**
 *
 * @author 041208085
 */
import java.util.*;
import java.io.*;
public class FootballOutput {

    /**
     * 
     */
    public static void main(String[] args) throws FileNotFoundException {
       // set variables for files
        Scanner inFile = new Scanner(new FileReader("footballdata.txt"));
        //set up program variables
        int ticketBox, boxNum, ticketSideline, sidelineNum, ticketPremium,premiumNum,ticketGeneral,generalNum,totalAmount;
        // reading the parameter from the file, set the data;
        ticketBox = inFile.nextInt();
        boxNum = inFile.nextInt();
        ticketSideline = inFile.nextInt();
        sidelineNum =inFile.nextInt();
        ticketPremium =inFile.nextInt();
        premiumNum =inFile.nextInt();
        ticketGeneral = inFile.nextInt();
        generalNum = inFile.nextInt();
        //calculate the totalAmount
        totalAmount = (ticketBox * boxNum) + (ticketSideline * sidelineNum) + (ticketPremium * premiumNum) + (ticketGeneral * generalNum);
        // close the files;
        inFile.close();
        // set variable for output files
        PrintWriter outFile = new PrintWriter("footballOut.txt");
        //output the record;
        outFile.printf("%d %d %n%d %d %n%d %5d %n%d %5d %ntotalAmount is %d  ",ticketBox,ticketBox * boxNum,ticketSideline,ticketSideline * sidelineNum,ticketPremium,ticketPremium * premiumNum,ticketGeneral,ticketGeneral * generalNum,totalAmount);
        outFile.close();
        
    }
}
