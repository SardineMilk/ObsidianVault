```
package fractions;

public class Fraction {
	private int numerator;
	private int denominator;
	
	public Fraction(int numerator, int denominator) {
		this.numerator = numerator;
		this.denominator = denominator;
	}
	public Fraction(int numerator) {
		this.numerator = numerator;
		this.denominator = 1;
	}
	
	public int getNumerator() {
		return this.numerator;
	}
	public int getDenominator() {
		return this.Denominator;
	}
	
	public void setNumerator(int numerator) {
		this.numerator = numerator;
	}
	public void setDonominator(int denominator) {
		this.denominator = denominator;
	}

	public String toString() {
		return this.numerator + "/" + this.denominator;	
	}

	public static void main(String args[]) {
		Fraction f1 = new Fraction(3,4);
		Fraction f2 = new Fraction(4);
		System.out.println(f2.getDenominator());
	}
}
```