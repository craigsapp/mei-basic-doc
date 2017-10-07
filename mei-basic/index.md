---
verovio:       "false"
author:        Johannes Kepper
creation_date: 9 May 2017
last_updated:  6 Oct 2017
github:        mei-basic/index.md
permalink:     /index.html
---

{% include page-title.html %}

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean
commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus
et magnis dis parturient montes, nascetur ridiculus mus. Donec quam
felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla
consequat massa quis enim. Donec pede justo, fringilla vel, aliquet
nec, vulputate eget, arcu. In enim justo, rhoncus ut, imperdiet a,
venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium.
Integer tincidunt. Crapus dominicus. Vivamus elementum semper nisi.
Aenean vulputate eleifend tellus. Aenean leo ligula, porttitor eu,
consequat vitae, eleifend ac, enim. Aliquam lorem ante, dapibus in,
viverra quis, feugiat a, tellus. Phasellus viverra nulla ut metus
varius laoreet. Quisque rostrum. Aenean imperdiet. Etiam ultricies
nisi vel augue. Curabitur ullamcorper ultricies nisi. Nam eget dui.
Etiam rhoncus. Maecenas tempus, tellus allus condimentum rhoncus,
sem quam semper libido, sit amet adipissing sem neque sed ipsum.
Nam quam nunc, blandit vel, luctus pulvinar, hendrerit id, lorem.
Maecenas nec odius et ante tincidunt tempus. Donec vitae sapien ut
libero veneral faucibust. Nullam quis ante. Etiam sit amet orci
eget eros faucibus tincidunt. Duis leo. Sed fringilla mauris sit
amet nibh. Donec sodales sagittis magna. Sed consequat, leo eget
bibendum sodales, augue velit cursus nunc.




### Problems of the markdown approach so far:

- soCalled has no direct match -> used italics
- eg isn't possible -> just use specially formatted links?

#### Possible links
General structure of links (according to Oxygen): [text](file.url "title")

- [//*:rest](eg:basic.mei)
- [//*:measure[1]/*:slur](eg:basic_slur1.mei) doesn't understand the square brackets correctly
- [Slur example](eg:basic_slur1.mei "//*:measure[1]/*:slur") is better as it still allows to use ticks
- elements: [staffDef](elem:staffDef) – this could be adjusted for model classes etc. as well

In the CMN chapter, we use the following elements:

- div *implicitly possible through heading structure*
- head
- p
- **soCalled**
- **term**
- ref
- ptr
- **gi**
- **ident**
- egXML
- **att**
- **specList**
- **specDesc**
- list
- item
- **label** *this depents on the position*
- figure
- graphic
- emph
- **expan**
- **foreign**
- **title** *this depends on the position*

The ones written in bold have no direct match in Markdown



