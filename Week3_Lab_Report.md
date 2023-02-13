# Researching Commands
### grep commands

- **grep -l**: Prints the names of the files which match the provided word.

#Example 1: grep -l looks through a group of files to find the word we are looking for.
```
$ grep -l "lighter" written_2/*/*/*.txt
written_2/travel_guides/berlitz1/WhatToMalaysia.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
written_2/travel_guides/berlitz1/WhereToMalaysia.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
```

#Example 2: grep -l does not return anything because the word is not in the given files.
```
$ grep -l "punctuation" written_2/*/*/*.txt
```
Helps to get all the files with the provided word.

- **grep -w**: Prints the lines in which the word is completely present.

#Example 1: grep -w looks through a group of files to find the exact word we are looking for.
```
$ grep -w "hatching" written_2/*/*/*.txt
written_2//travel_guides/berlitz1/WhereToEdinburgh.txt:        the zoo celebrated the first successful hatching in captivity of a king
written_2//travel_guides/berlitz2/Bali-WhereToGo.txt:Farther south, the dry scrub-covered hills slowly give way to semi-desert, with an occasional grove of coconut palms playing the role of oasis. Energetic resurfacing and new construction has transformed the road, but Kuta Beach is still far from resembling its namesake in Bali. Most of the time, its white coral sands are largely deserted. Most accommodations are still in simple cottages, some with a modest restaurant as well. Otherwise you can find a cheap warung. Novotel’s Mandalika Resort, designed to resemble a Sasak Village by the sands of Kuta Beach, is the one upscale vacation complex in the area. Hotels in the area can arrange transportation to some of the beautiful, isolated beaches nearby. The Sunday morning market at the hamlet of Kuta is lively and interesting. Once a year in February or March, a few days after the second full moon of the year, crowds gather on the beach for Bau Nyale. The all-night festival is timed to coincide with the hatching of strange worms from the sea bed.
written_2//travel_guides/berlitz2/Canada-WhereToGo.txt:The National Museum of Science and Technology (1867 St. Laurent Boulevard) is in the style of science through fun and games. In Canada’s largest museum, there are views of the heavens through a huge refracting telescope, do-it-yourself demonstrations of balance and optics, and a plastic bubble with live chicks hatching in front of your eyes. But with all the new-fangled razzmatazz, the museum hasn’t forgotten the charm of mint-condition antique cars and, above all, old train engines — behemoths from the great era of steam that truly “made” Canada.
```
#Example 2:
```
$ grep -w "hatch" written_2//*/*/*.txt
written_2//travel_guides/berlitz2/Vallarta-WhatToDo.txt:Another seasonal, and very worthwhile eco-conscious activity, is to participate in the nightly sea turtle releases and watches that take place from August through November along the shores of Banderas Bay, and further south in Mazunte (located between Huatulco and Puerto Escondido). Preservation groups and trained specialists conduct these releases and watches. You participate by helping to collect the turtles’ eggs and taking them to a safe nesting area for incubation. After the baby turtles hatch, they are released back into the ocean. Organized visits to the turtle camps are conducted daily in Mazunte, at the Centro Mexicano de la Tortuga, and in Puerto Vallarta by several of the beachfront hotels and a select group of ecologically oriented tour operators, such as Eco-tours de México (Tel. (3) 222-6606).
```
If I had just searched for grep "hatch", it would have given me files containing all other words that have hatch. Eg. thatched, hatchery.

- **grep -c**: Prints the count of the number of times the given word appears in all text files of the given path.

#Example 1: gives the number of times "high" appears in the files.
```
$ grep -c "high" written_2/*/*/Rybczynski/*.txt
written_2/non-fiction/OUP/Rybczynski/ch1.txt:5
written_2/non-fiction/OUP/Rybczynski/ch2.txt:8
written_2/non-fiction/OUP/Rybczynski/ch3.txt:8
```
#Example 2: gives the number of times "lighter" appears in the same set of files.
```
5$ grep -c "lighter" written_2/*/*/Rybczynski/*.txt
written_2/non-fiction/OUP/Rybczynski/ch1.txt:0
written_2/non-fiction/OUP/Rybczynski/ch2.txt:1
written_2/non-fiction/OUP/Rybczynski/ch3.txt:2
```
- **grep -i**: Ignores the case of the word we give.

#Example 1: Even though the provided word was "Expert" the search results include files containing "expert".
```
grep -i  "Expert" written_2/*/*/Rybczynski/*.txt
written_2/non-fiction/OUP/Rybczynski/ch2.txt:The Empire State Building has one whimsical touch. The final plans called for the skyscraper to end with a flat roof over the 85th floor—1,050 feet, precisely calculated to be two feet higher than the top of the Chrysler Building’s spire. Then, before construction began, the owners decided that two feet was not enough, and ordered the architects to add a 200-foot tower to the top of the building.* This was to be not merely a decorative spire but a functioning symbol of the modern age, a mooring tower for airships. Instead of dropping transatlantic travelers off at Lakehurst, N.J., the thousand-foot-long dirigibles would fly right into Manhattan and hook themselves up to the top of the Empire State Building. Passengers would disembark to an observation platform and descend by elevator to a lounge and customs area on the 86th floor. Most experts, including Hugo Eckener, commander of the Graf Zeppelin, doubted that it could be done. It was hard enough to dock the unwieldy leviathans at ground level, never mind 1,250 feet up in the air. The experts proved to be right, and no airship passengers ever landed atop the Empire State.1 Yet the rocket-shaped tower, with its cast aluminum buttresses and gleaming conical top, is the perfect fanciful crown for this rather solemn skyscraper.
written_2/non-fiction/OUP/Rybczynski/ch3.txt:When an architectural competition was announced for the New York Public Library on May 21, 1897, Dr. John Shaw Billings, the library’s executive director, was determined that in his building, design would not triumph over function. He had in mind Boston’s newly built public library, a beautiful but in his opinion poorly functioning building. Billings, an ex-army physician, was responsible for organizing the Surgeon General’s Library and a celebrated medical index. He was also an expert in hospital design, and was thus familiar with building construction. He drafted a plan for the new library whose most unorthodox feature was the location of the main reading room. It was not located near the main entrance, as was common practice, but on an upper floor, above the book stacks.
```
#Example 2: 
```
$ grep -i  "entities" written_2/*/*/Berk/*.txt
written_2/non-fiction/OUP/Berk/CH4.txt:Yet in make-believe, children use objects to symbolize things that are very different from the objects themselves—a ball to stand for an apple, a laundry basket for a cradle. They do not judge these imaginary symbols to be real, so clearly they can tell the difference between pretend and real experiences long before they can answer many appearance–reality problems correctly.36 The more 3- to 5-year-olds spontaneously engage in joint make-believe with classmates at preschool, the better they can distinguish the apparent and real identities of disguised objects.37 Pretending with peers may help children master appearance– reality distinctions because it offers repeated practice in transforming a wide variety of objects from their real state to a pretend state and back again.
written_2/non-fiction/OUP/Berk/CH4.txt:By observing children’s play themes, we can discover much about the values and identities that our culture—by way of homes, child-care centers, schools, and community youth activities—transmits to the next generation. As leaders in children’s development, parents and teachers are in a prime position to design and inﬂuence children’s play worlds in ways that shield them from acquiring materialistic and violent attitudes and behaviors and that accentuate play’s cognitive, emotional, and social beneﬁts. Vygotsky’s theory reminds us that as long as we think carefully about the play materials we offer, the style and content of adult–child play, and the social skills we encourage in children’s peer relations, make-believe play can nurture a wide range of capacities essential for academic, social, and later-life success.
written_2/non-fiction/OUP/Berk/ch1.txt:According to Vygotsky, infants are biologically endowed with basic perceptual, attentional, and memory capacities that they share with other animals. These undergo a natural course of development through direct contact with the environment during the ﬁrst two years of life, similar to the process of exploration and discovery described by Piaget. For example, all babies gradually distinguish objects and people in their surroundings and realize that these entities continue to exist when out of sight. They also merge objects that are alike into categories (such as vehicles, animals, birds, and eating utensils), laying the foundation for mentally representing their experiences and thinking eciently. And they become adept at imitating others, a powerful means for acquiring new skills. These and other infant capabilities set the stage for language, which develops with extraordinary speed after 1 year of age. By ages 2 to 3, most children are skilled conversationalists; by age 6, they have mastered most of the grammatical rules of their language and have vocabularies as large as ten thousand words.81 
```
If we forget the case of the word, this could help us find the word in the files.



Sources:
- grep --help
