# Tag Generator

I wanted a way to display tags for skills in a HTML-based resume. I also wanted all of the HTML, CSS, and Javascript in the same file.

<video autoplay muted loop playsinline src="https://github.com/user-attachments/assets/6dfa05f6-fd5f-4d84-a24b-479832e82abe" type="video/mp4" />

https://github.com/user-attachments/assets/6dfa05f6-fd5f-4d84-a24b-479832e82abe

In this initial version I wanted to stay away from using loops within loops to separate out the text from the delimiters.

The idea I started with in this revision was to find the indices of the delimiters and then only take the strings between those points. This was simple enough, but I wanted to account for the possibility of the delimiters being more than 1 character, so I adjusted the logic slightly to mark the indices of the start and end of strings without delimiters.

With multiple delimiter types allowed, we still need to loop through this process for each delimiter, then combine the indices.

Because the method requires 2 indices - start and end of the string - an even number of delimiters can cause an issue with the combining process. To get around this, the current solution removes the first and last indices from the combined array if the delimiter list is an even number.

In the next iteration I will use a recursive approach when stepping through the delimiters.

While the idea was to have everything in one file, so it could be portable, for the sake of exploring this functionality I will break up the JS into separate files.
