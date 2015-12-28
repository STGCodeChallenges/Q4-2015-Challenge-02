#Challenge #2 (due 11/30/2015): SOLID Shipping Calculator
Inspired by the Strategy Pattern from [this Pluralsight course](http://app.pluralsight.com/library/courses/patterns-library/table-of-contents), I thought it would be nice to review how to refactor code that breaks basic [SOLID principles](http://app.pluralsight.com/courses/principles-oo-design).

##Description
With Black Friday around the corner, we wanted to create a shipping calculator that compares the various shipping methods to determine the final cost; however, we quickly realized that our core CalculateShippingCost()method is becoming unwieldy as new shipping options are added.  More importantly, it’s breaking the open-closed principle of SOLID software development.  Your task is to completely eliminate the switch statement in the pseudo code below so that future shipping options can be added in the future with much greater ease:

```
public double CalculateShippingCost(Order order) {
	switch (order.ShippingMethod) {
		case "UPS": return CalculateUpsShipping();
		case "FedEx": return CalculateFedExShipping();
		case "USPS": return CalculateUspsShipping();
	}
}
```

Simply changing the switch statements to some form of an if/else is also not allowed.  Feel free to stub out dummy implementation for the rest of the code (i.e. the Order class, the various shipping method calculations, etc.), as the purpose of this exercise is more focused on how to refactor the code, rather than providing a full implementation.

##Bonus Entry
As expected, we need to add another shipping method, DHL.  Add this to your list of shipping methods without modifying the core CalculateShippingCost() method.  As before, feel free to stub out dummy implementation details.

##Submission Instructions

GitHub repo: https://github.com/STGCodeChallenges/Q4-2015-Challenge-02

Google Form (to be filled out upon completion of challenge): https://docs.google.com/a/stgconsulting.com/forms/d/1tWiVzb6cq9qftcGuKT4APOIW5Zh83iaJLmHdEXkZcV4/viewform?usp=send_form
