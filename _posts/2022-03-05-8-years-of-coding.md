---
layout: post
title:  "8 Years of Coding"
date:   2022-03-05 09:58:00 -0700
categories: blog
---
### 2013 - 2014
At the end of my junior year of high school they gathered a limited group of students (not sure how they determined who got to be in the group) to discuss a new course offering, AP computer science. I was intrigued though really not sure what computer science was, even after this meeting. I had a vague notion of what programming was but no one in my life was a programmer or software engineer so I had not really been exposed to it. Nevertheless, I signed up for the class.

Most of the work we did in the class revolved around [Karel J Robot][karel-j]. Big daddy Karel (pronounced Karl) was a robot that lived on a grid and you controlled Karel’s movements by calling functions like turnLeft, turnRight, and moveForward. Karel J was supposed to be an easy introduction to object oriented programming but I remember being very confused about how Karel actually worked. Not how to move Karel around the grid. That was painfully easy. But how did Karel’s image and the grid get rendered on the screen? What was happening when you called the function moveForward and how was that connected to the Karel J sprite? Where was Karel’s current state stored? I didn’t even know enough about object oriented programming to formulate these questions. If we had dived into these topics I would have been much more interested but my conception of programming was that I could make Karel move around the grid and not much else, which seemed pretty useless.

One exercise we did that was unrelated to Mr. Karel J Robot was taking an integer and printing the individual digits (not sure what order so lets say from least to most significant). At the time I thought this was a pretty tough challenge but I was able to solve it. Today my solution would look something like this.

```java
import java.util.Scanner;

public class PrintDigits {
	
	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);
		System.out.print("Enter a number: ");
		int n = scan.nextInt();

		while (n) {
			System.out.println(n % 10);
			n /= 10;
		}
		scan.close();
	}
}
```

I’m not actually sure if we learned about the modulus operator because I just remember using integer division which has truncation to get the values I wanted. It’s possible we did learn modulus and I just didn’t see how modulus could be used to solve this easily. Back then my code may have looked like this.

```java
import java.util.Scanner;
public class NoobPrintDigits {
	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);
		System.out.print("Enter a number: ");
		int n = scan.nextInt();
		while (n != 0) {
			int a = n / 10;
			System.out.println(n - (a * 10));
			n = a;
		}
  }
}
```

Honestly I am sure it was much worse than this but I can’t bring myself to un-optimize it further. I probably used a lot more unnecessary divisions and bad indentation. I left out the line that closes the scanner because there’s no way I did that back in the day.

I wish I could say that as a result of this class I fell in love with programming and realized its true power and potential but I really cannot. I don’t want to blame it entirely on the class — I certainly could have taken the class more seriously and I was exposed to enough concepts and ideas that I could have gone off on my own and really learned how to program — but with hindsight it is clear to me this class was not taught well. It is not that surprising given the fact that this was the first year the course was offered at my school, the teacher had very little programming experience, and the experience he did have was in Visual Basic many years before. I had a lot of friends in this class, it was at the end of the day, and there were very few days where the teacher actually had a lesson planned so the class kind of felt like a social hour. I actually really enjoyed the class because it was low stress and I got to talk to a lot of my nerdy friends but unfortunately I did not learn much.

In the weeks before the AP exam it became clear that I was woefully underprepared and I spent one or two evenings just reading the textbook straight through without doing any exercises. This is absolutely not the best way to learn but I will say it was eye opening to read the text book for the first time and this was maybe my first glimpse at what programming actually was. I can recall coming back to my classmates after my long foray into the fundamentals of Java and claiming that programming was actually super interesting. To be clear we had a few assigned readings from the textbook over the course of the year but it was not a big part of the class. Also I was a bad student and did not do the readings.

On the day of the AP exam I felt unprepared, because I was, and I remember the test being difficult but not absurdly so. I don’t think the coding questions were difficult but it was hard for me to answer some multiple choice questions because I simply had not learned the relevant topics. Sadly, I got a 4 on the exam.

That pretty much sums up my first year of programming! A bit underwhelming, I know. But very soon fledgling (/ˈflejliNG/ noun - a young bird that had just fledged.) Duncan would discover how awesome programming actually is 😁. 

### 2014 - 2015

My freshman year of college I decided to study math and one of the requirements for pure math majors was to take an Intro to Programming class. I went ahead and took the class my first semester because I figured it would be prudent to get it out of the way while the little knowledge I had from the previous year was still fresh.

The instructor for the class, Melina Vastola, was an amazing teacher. She was extremely enthusiastic, a great explainer, and it was clear she really cared about the success of her students. She ignited my interest and love for coding and I just want to highlight her as an example of how a great teacher can change the course of someones life. She shows up later in my story as well.

*Note: The core CS classes at FSU were taught in C++, which is still my favorite programming language although I do find myself using other languages like Python and Javascript more often nowadays. Java remains my least favorite language and its popularity baffles me.*

In the spring semester of my freshman (I had to look up the correct usage of freshman vs freshmen: when using as an adjective always use the singular form, freshman) year I signed up for Object-Oriented Programming with another fantastic instructor, Bob Myers. This guy was a performer. Going to one of his lectures felt like watching a play, in a good way. The lessons were perfectly orchestrated and the only indication that he was not a prerecorded hologram precisely executing a script was the fact that he would take questions. Not to my surprise, I found out later he was actually a thespian. It was because of this energy that I wanted to do really well in the class. I wanted him to recognize my face and that I was a good student when he handed me back my exams.

I don't remember many specifics from either class, probably due to the fact that I TA'ed for both of these classes during grad school and have mixed up a lot of the curriculum between when I was a student and a TA for the course. I know one of our assignments in OOP was to write a string class similar to the string in the C++ standard library, with a subset of the functionality.

```cpp
// This is my code but unfortunately not for that assignment.
// My laptop with all my code from undergrad was stolen :(
class String {
	
	friend std::ostream& operator<<(std::ostream &os, const String &s);
	friend std::istream& operator>>(std::istream &is, String &s);
	friend String operator+(const String &a, const String &b);

	public:
		String();
		String(const char *s);
		String(char c);
		String(const String &s);
		~String();
		String substring(size_t pos = 0, size_t len = npos) const;
		char operator[](size_t i) const;
		const String& operator=(const String& s);
		bool operator==(const String &s) const;
		const char* cstring() const;
		size_t len();
		void shrink();
	
	private:
		void grow();
		char *cstr;
		size_t size, max;

		static const size_t npos = -1;
};
```

There is something about a truly great teacher that is inspiring to me. Bob and Melina both were exceptionally passionate and good at their jobs and it was because of them that I started wondering what it would be like to teach. Could I ever inspire a group of students in the same way?





[karel-j]: https://csis.pace.edu/~bergin/KarelJava2ed/Karel++JavaEdition.html