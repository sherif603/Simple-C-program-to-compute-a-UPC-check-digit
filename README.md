# Simple-C-program-to-compute-a-UPC-check-digit
## Compute the universal product code (UPC) check digit with C
The Universal Product Code (UPC) is a series of black bars or lines that help identify a product. this symbol is encoded with a series of numbers known as the Global Trade Item Number (GTIN), which together a GTIN and a UPC are the two elements that make up the complete barcode. The UPC is scanned by special optical scanners called barcode readers at the point of sale, along with these lines and digits. they make up the barcode and allow systems to properly identify items look up their price and automatically transmit information about the product to a computer.
A proper UPC, along with additional information such as batch or lot numbers, allows a company to recall damaged items accurately and easily from a retailer, distributor, or warehouse before they reach the public without a valid UPC, tracking and selling your inventory through the supply chain is not possible. UPC allows proper sales forecasting for your product as you can accurately calculate current inventory, products sold, and demand.
The UPC is printed on most items sold in supermarkets and other mass retailing outlets all over the United States of America and Canada. Each barcode represents a twelve-digit number, usually printed underneath the bars. For example, the following barcode [0,13800,15173,5] comes from a manufacturer: Stouffer's, category: Food, Beverages & Tobacco, and a package of Stouffer's French Bread Pepperoni Pizza.
## The Calculation of the final digit of the barcode, the Check Digit:
The digits [0,13800, 15173,5] appear underneath the barcode consisting of the first digit (0) identifies the type of item (0, 1, 6, 7, and 8 for most items, 2 for items that must be weighed e.g. meat, 3 for drugs and related merchandise, 4 for in-store marking of non-food items, 5 and 9 for coupon use), the first group of five digits identifies the manufacturer (13800 is the code for Nestle USA's Frozen Food Division), the second group of five digits identifies the product (15173 is the code of Stouffer's French Bread Pepperoni Pizza), and the final digit is a "check digit," whose only purpose is to help identify an error in the preceding digits.
If the UPC is scanned incorrectly, the first 11 digits (0,13800,15173) probably won't be consistent with the final digit (5), and the store's scanner will reject the entire code. Here's a method of computing the check digit:
Add the first, third, fifth, seventh, ninth, and eleventh digits [0 + 3 + 0 + 1 + 3 = 8]. Add the second, fourth, sixth, eighth, and tenth digits [1 + 8 + 0 + 5 + 7 = 21]. Multiply the first sum by 3 and add it to the second sum [(8 * 3) + 21 = 45]. Subtract 1 from the total [45 - 1 = 44]. Compute the remainder when the adjusted total is divided by 10 [4}. Subtract the remainder from 9 [9 - 4 = 5].
## The Objective:
Write a C program that computes the Check Digit for an arbitrary UPC.
## The Requirements:
### Source Code
Plain text file.
Can use any text editor to create this file.
The contents are written in a C programming language using the language's rules, syntax, and formatting.
Ends with the .c file extension.
Contains programming instructions.
### Object Code
Compiled from the source code file.
The C language compiler.
Contains tokenized instructions.
Ends with the .o file extension, and they use the same file name as the source code file.
### The Linker
Often done as part of compiling.
Combines object code and C library file.
Create a binary, executable file.
### Command Prompt Development
Editor.
Compiler.
Linker.
### Integrated Development Environment (IDE):
The Code::Block is a free, open-source, cross-platform C, C++, and Fortran IDE built to meet the most demanding needs of its users.



