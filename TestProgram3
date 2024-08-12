package com.example.project;

import static org.junit.jupiter.api.Assertions.assertEquals;

import org.junit.jupiter.api.DisplayName;
import org.junit.jupiter.api.Test;
import org.junit.jupiter.params.ParameterizedTest;
import org.junit.jupiter.params.provider.CsvSource;

import java.io.*;

public class TestProgram3 {

   @Test
   public void test1()
   {
     PrintStream originalOut = System.out;
     ByteArrayOutputStream bos = new ByteArrayOutputStream();
     System.setOut(new PrintStream(bos));

     InputStream originalIn = System.in; // backup System.in to restore it later
     ByteArrayInputStream in = new ByteArrayInputStream("143\n82".getBytes());
     System.setIn(in);

     // action
     Program3.main(null);

     // assertion
     assertEquals("The length is 143\nThe width is 82\nThe area is 11726\nThe perimeter is 450", bos.toString());

     // undo the binding in System
     System.setOut(originalOut);
     System.setIn(originalIn);
   }
}
