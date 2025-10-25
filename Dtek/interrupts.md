
för att inte ex behöva polla värden hela tiden
fins (exmepelvis för en board) Core Local interuptor som hanterar timer och software interrupts, och en Platform level interrupt controller (PLIC) som samlar interrupts från andra peripherals

hoppar till en interrupt handler när händer och sedan tillbaka till där man var i instruktionerna

finns CSR registers relaterade till CLINT, ex mtvec mie mstatus