# Grand-Circus
Deliverables

package com.company;

import java.util.Scanner;


public class Main {

    public static void main(String[] args) {

        //initialize
        int first_date = 0;
        int second_date = 0;
        int numdays = 0;

        //get total number of hours that have passed up to this date
        first_date = calchours();
        second_date= calchours();

        //the difference of hours passed converted back to number of days
        if (first_date > second_date){
            numdays = (first_date - second_date)/24;
        }else {
            numdays = (second_date - first_date)/24;
        }

        System.out.println("Number of days between: " + numdays);

    }

    public static int calchours(){

        //initialize
        int month = 0;
        int day = 0;
        int year = 0;
        int mhours = 0;
        int dhours = 0;
        int yhours = 0;
        int date = 0;

        Scanner inYear = new Scanner(System.in);
        Scanner inDay = new Scanner(System.in);
        Scanner inMonth = new Scanner(System.in);

        //Month numerical input
        System.out.println("Enter Month: ");
        month = inMonth.nextInt();

        //Day numerical input
        System.out.println("Enter Day: ");
        day = inDay.nextInt();

        //Year numerical input
        System.out.println("Enter Year: ");
        year = inYear.nextInt();

        //Hours in months: the number of hours in all the months previously completed.
        // i.e the number of hours in march is all of the hours in jan + feb up to the day of march
        switch (month) {
            case 1:
                mhours = mhours + 0;
                break;
            case 2:
                mhours = mhours + 31 * 24;
                break;
            case 3:
                mhours = mhours + 59 * 24;
                break;
            case 4:
                mhours = mhours + 90 * 24;
                break;
            case 5:
                mhours = mhours + 120 * 24;
                break;
            case 6:
                mhours = mhours + 151 * 24;
                break;
            case 7:
                mhours = mhours + 181 * 24;
                break;
            case 8:
                mhours = month + 212 * 24;
                break;
            case 9:
                mhours = mhours + 243 * 24;
                break;
            case 10:
                mhours = mhours + 273 * 24;
                break;
            case 11:
                mhours = mhours + 304 * 24;
                break;
            case 12:
                mhours = mhours + 334 * 24;
                break;
        }

        //day and years to hours
        dhours = day * 24;
        yhours = (year * 365) * 24;

        //total amount of hours for this date
        date = mhours + dhours + yhours;

        return date;
    }

}
