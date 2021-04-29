
Given a large number of binary files, write a program that finds the
longest strand of bytes that is identical between two or more files

Use the test set attached (files sample.*)

The program should display:
- the length of the strand
- the file names where the largest strand appears
- the offset where the strand appears in each file

import java.io.*;

public class Binary {
    public static void main(String args[]) throws IOException
    {
        if(args.length < 2)
        {
            System.out.println("Provide input file to read");
            System.exit(0);
        }
        String inputFile = args[0];
        try {
            
            FileInputStream inputStream = new FileInputStream(inputFile);
            long length = file.length();
            byte[] bytes = new byte[(int) length];
            inputStream.read(bytes);
            inputStream.close();
            String s = new String(bytes);
            System.out.println(s);
        }
        catch (IOException e)
        {
            System.out.println(e);
        }
    }
}
