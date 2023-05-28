## What is an algorithm ?
Algorithm is simply **problem-solving-steps**.

Imagine trying to find a name in a phone-book;
- You can start searching from first page until you find your searched name. But this approach can take a long time.
- You can search 2 pages at a time, and if you passed the name, you go back one.
- However, there is another way, you can start at the middle of the book, then you look at the name that you find, if it's not the name you're looking for, you ask a question "Is it on the left side of the book, or right?", then you divide the half of the remaining phone book until you find your name.
Each of these approaches are called an **algorithm**.

The speed of each of these algorithms can be pictured as this chart, which is called **big-0 notation**;
![[big-0-notation.png]]

- Red line is the first algorithm and it has a **big-0** of **n** because if there is 100 names, it takes 100 steps to find the correct name.
- Yellow line is the second algorithm, where 2 pages searched at a time, it's **twice as fast from the red line**, so it takes **n/2** time to find the correct name.
- Green line is the last algorithm, where you divide the remaining book, if you double the size of the phone book, only one step added. So it's **log<sub>2</sub>n** speed.