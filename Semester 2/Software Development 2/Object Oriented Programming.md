```
package fractions;

public class Fraction {

    private int numerator;
    private int denominator;
    

	public Fraction(int numerator, int denominator) {

	    this.numerator = numerator;
	    if (denominator == 0) {
	        throw new IllegalArgumentException("The denominator cannot be 0");
	    } else {
	        this.denominator = denominator;
	    }
	}

    
    public Fraction(int num) {
        numerator = num;
        denominator = 1;
    }
    
    public void setNumerator(int numerator) {
        this.numerator = numerator;
    }
    
    public int getNumerator() {
        return numerator;
    }
    
    public void setDenominator(int denominator) {
        this.denominator = denominator;
    }
    
    public int getDenominator() {
        return denominator;
    }
    
    public String toString() {
        return numerator + "/" + denominator;
    }
    
    private static int gcd(int m, int n) {
        int a = m;
        int b = n;
        int remainder;
        while (b != 0) {
            remainder = a % b;
            a = b;
            b = remainder;
        }
        return a;
    }
    
    private void simplify() {
        int g = gcd(numerator,denominator);
        numerator = numerator/g;
        denominator = denominator/g;
    }
    
    public Fraction multiply(Fraction f) {
        int num = this.numerator * f.getNumerator();
        int den = this.denominator * f.getDenominator();
        Fraction g = new Fraction(num,den);
        g.simplify();
        return g;
    }
    
    public Fraction add(Fraction f) {
        int num = this.numerator * f.getDenominator() + f.getNumerator() * this.denominator;
        int den = this.denominator * f.getDenominator();
        Fraction g = new Fraction(num,den);
        g.simplify();
        return g;
    }
    
	public static Fraction parseFraction(String frac) throws ParseException {
	    int num, den;
	    String[] splitFrac = frac.split("/");
	    if (splitFrac.length != 2) {
	        throw new ParseException("Invalid fraction: does not contain only one slash", 0);
	    } else {
	        try {  
	            num = Integer.parseInt(splitFrac[0]);
	            den = Integer.parseInt(splitFrac[1]);
	        } catch(NumberFormatException e){  
	            throw new ParseException("Invalid fraction: does not contain only numbers", 0);
	        }  
	    }
	    return new Fraction(num, den);
	}


	public boolean equals(Object o) {
	    Fraction f = (Fraction) o;
	    return this.getNumerator() * f.getDenominator() == this.getDenominator() * f.getNumerator();
	}


    public static void main(String[] args) {
        Fraction f1 = new Fraction(1,4);
        Fraction f2 = new Fraction(1,4);
        System.out.println(f1.add(f2));
    }
}

```