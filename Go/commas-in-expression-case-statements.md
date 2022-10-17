---
title: Commas in Expression Case Statements
type: tidbit
---

The use of comma in case statements work for expression:

	x := 2

	switch {
	case x == 1, x == 2:
		fmt.Println("x < 3")
	default:
		fmt.Println("x >= 3")
	}

If `x` is 1 or 2, the `x < 3` will be printed out.
