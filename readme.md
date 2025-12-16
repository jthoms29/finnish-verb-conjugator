A simple Finnish verb conjugator made as a final project for Linguistics 349 with Dr. Jesse Stewart

Given a verb in its infnitive form, this outputs the present tense as well as negative imperfect (past) tense.
### Verb Types
Based on a Finnish verbs infinitive form, there are six possible verb types it can be classed as based on its ending
- Type 1: Ends with two vowels
- Type 2: Ends with a 'd' then 'a/ä'
- Type 3: Ends with two cononants then a vowel
- Type 4: Ends with a vowel, 't', then a/ä
- Type 5: Ends with 'it' then a/ä
- Type 6: Ends with 'et' then a/ä

How the verbs are conjugated depends on which class they are in.
Most of how this is implemented is based on the verb conjugation rules outlined here - https://uusikielemme.fi/


### Consonant gradation
When conjugating a Finnish verb, sometimes the word will undergo consonant gradation, meaning that
certain consonants within the word will change. There are two versions - weak gradation and strong gradation, and
different verb types switch between different versions.
This gradation only occurs on the border of the second-to-last and last syllable for the verb's infinitive root,
so I that is taken into account. There are other rules outlined in the link above, including certain clusters of consonants that never change.

## Issues
Irregular forms aren't accounted for the most part. Most of the present issues come from irregularities in consonant gradation.

In type 2 verbs, there are some irregular forms that I didn't check for, as such they 
won't undergo consonant gradation correctly.


Certain verb types go from a weak form in the infinitive to a strong form when conjugated
This brings up an issue that isn't present when going from strong to weak.

When going from strong to weak, there are some instances where a 'k' in the infinitive form is removed.
The opposite is also true, sometimes when going from weak to strong a 'k' is added to the verb. Where this
happens seems to depend on historical versions of these verbs that aren't really used in modern Finnish, so
there's no concrete rules I can use to know when a K will be added.

As such, type 3, 4, and 6 verbs may not be correct. For example, The first-person singular form of 'juosta' should be 'juoksen', but
here the output here is 'juosen'.


Most type 4 verbs undergo consonant gradation, but there are some irregular forms that don't. There's 
no real pattern to which ones don't. For example, the first person singular form of 'avata' should be
'avaan', but the output here is 'apaan'.