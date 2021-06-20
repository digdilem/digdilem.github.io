---
layout: page
title: Redneck water cooling
subtitle: Water cooling servers using household plumbing
---

"How to water cool computers using household plumbing equipment"

I like peace and quiet. Most water cooling rigs available for home PCs are anything but - they only use water to move the heat away from the CPU and GPU to a finned radiator, then blast it with fans. I thought that radiant cooling would work and not need any fans, so I built a water cooling system. It worked perfectly for a linux server and my gaming windows PC for three years, until I had to free up space and instead focussed on sound proofing a cupboard and using air cooling. This was back in 2010 but there's no reason why it wouldn't work today. 

# The plan

![draft1-1200x661](https://user-images.githubusercontent.com/4052275/122675165-13c4cf00-d1d0-11eb-8986-c661835bc1d0.jpg)

This shows the initial plan of using a 22mm to 10mm 4-way adapter. In practice, my piping leaked here, so I used a flow and return circuit of 22mm copper, reducing to 15mm and then onto flexible pipe

# The equipment

![pump](https://user-images.githubusercontent.com/4052275/122675370-f7756200-d1d0-11eb-908f-1a903b7d54f7.jpg)
![rad-300x300](https://user-images.githubusercontent.com/4052275/122675372-f9d7bc00-d1d0-11eb-9bd0-b53fb0ad8d17.jpg)
![pipe1](https://user-images.githubusercontent.com/4052275/122675378-fe9c7000-d1d0-11eb-81c2-949bfe9941d8.jpg)
Plus various 15mm compression fittings - all standard UK wet central heating equipment. I had all this laying around from various DIY projects.
The only non-standard bit were the CPU and GPU heatsinks. They cost around £10 each, second hand from ebay. 

Total additional cost was about £95 - this was for the radiator, pipe and the heatsinks.

- The pump is a standard UK central heating pump. These are ceramic and designed to run 24/7 pumping water up to 80'c and use around 25 watts at speed setting 1 of 3. 
- The radiator is a small standard single pane radiator. This barely ran above room temperature (whgich is 15-30c), so oversized was it. It could have coped with at least six CPUs and GPUs. Bear in mind that all the piping is also radiating away heat, so by the time it gets to the rad it's already dropped a few degrees.


# Test fitting it in the garage

![DSCF1124](https://user-images.githubusercontent.com/4052275/122676763-563dda00-d1d7-11eb-8ab4-86b10e2ee73f.jpg)

To explain this:  The black plastic tank is the "header", containing water to fill the white pipe and allows and air in the system to vent. Fresh tap water contains a surprising amount of air which takes time to settle out. This tank needn't be as big as this - but I had this spare. 

Then water flows IN to the red central heating pump. Having the air vent before this allows much of the air to escape before hitting the pump. This causes about the only noise this system creates and lowers efficiency of the pumping, since the bubbles act as little pressure-absorbers. Handbooks will tell you about cavitation risk here, which might damage the impeller, but I consider this risk very small given the speed and low temperature of this water. But it's still good to avoid anyway.

Then water leaves the pump and into the radiator. Both inlet and outlet of this rad is on the bottom, so some air will collect at the top and can be bled away with a normal radiator key. (Once running for a while, the water loses its air content and no further bleeding will be needed until you introduce fresh water - just like a wet central heating system)

After the radiator, the water would go to the "Cold" side of the 15mm copper manifold (not shown here), and after passing through the heatsinks, would return to the "Hot" manifold, then back to the start of this loop.

![DSCF1135](https://user-images.githubusercontent.com/4052275/122676776-60f86f00-d1d7-11eb-8eec-564feca6baf2.jpg)

This shows one of the heat sinks being tested for pressure and stepping down in pipe sizes. Note the metal sleeves inside the joint - this worked well. Warming up the pipe ends in a cup of hot water allowed them to soften enough to form a snug fit.

![DSCF1143](https://user-images.githubusercontent.com/4052275/122677120-d153c000-d1d8-11eb-8cf3-8ce6aa7f2496.jpg)
![DSCF1136](https://user-images.githubusercontent.com/4052275/122677086-9ce00400-d1d8-11eb-971b-308d8fd36c10.jpg)

This shows one manifold created for two computers. Then the return flow speed from one block. It's not much, but doesn't need to be.

Overall these tests in a safe place were very useful to gain an understanding of how best to get this running together.

# Fitting it together in place

![DSCF1161](https://user-images.githubusercontent.com/4052275/122677144-f6e0c980-d1d8-11eb-9a02-590b24dcc9fe.jpg)

This shows the header tank and radiator in position, and the manifolds present on the lower right hand side inside a cupboard. You can see the clear pipes leading up from them to the computers above. (Stained red from a relatively small amount of rust in the system. This didn't affect operation and turned out just to be a thin coating on the pipes, with clear water after a few days)

![DSCF1165](https://user-images.githubusercontent.com/4052275/122677203-38717480-d1d9-11eb-9192-5f0345903cb6.jpg)

This is my linux server running very naked. You can see the flexible pipe coming into the cpu block. The hdd's are on elastic to reduce vibration noise.  I still run naked machines nowadays, even with cpu fans, as I have a nice soundproof place to put them. Cases aren't needed if you can limit physical access, and this removes the need for a case fan entirely, as non-hotspot sources of heat radiate upwards naturally.

![Installed-4](https://user-images.githubusercontent.com/4052275/122677266-8e461c80-d1d9-11eb-9c65-af9ea0f11485.jpg)
A close-up of the manifolds. Cold comes in from the radiator, Hot leaves to the pump. Each vertical section has a service valve that allows you to isolate supply entirely for one computer without affecting the other.

![legion](https://user-images.githubusercontent.com/4052275/122677317-c9e0e680-d1d9-11eb-99f4-4f98125f0420.jpg)
This was my windows PC< a gaming computer. Here the Cold supply comes into the blue CPU heatsink and then leaves to feed the GPU heatsink before returning to the Cold manifold. My view was that it's more important to cool the cpu first, but in reality the flow was enough so that it didn't really matter. The GPU didn't run much hotter than the CPU.

![legionblock_test](https://user-images.githubusercontent.com/4052275/122677379-fb59b200-d1d9-11eb-8f13-eb7fd7bf02d0.jpg)
This shows the same heatsinks before fitting them, so I could test for leaks and flow.

# Results
![Clipboard01](https://user-images.githubusercontent.com/4052275/122677441-23e1ac00-d1da-11eb-9d67-0a5bcb37afc8.jpg)

And some test results. This was a 2-core CPU running 'stress' to give some load, and as you can see the cpu temps are barely above ambient. I don't think this machine ever went above 30'c cpu temp during the several years of this operation.

# Thoughts
I enjoyed this project and the benefits it brought for several years. The pump never failed and was almost silent in operation (except for air bubbles and the very faintest hum). I never had a leak nor lost any failures, but obviously that is a risk with any wet system. The biggest noise was the PSU fan, but with 120mm fans and choosing 'quiet' models I deemed it acceptable. 

Eventually I upgraded the GPU on my gaming PC and I couldn't find a compatible water block for it (remember this was before water cooling was as popular as it is now) and so I regretfully removed the kit. I replaced the linux server with an HP ML110 which went in an outbuilding, so that was no longer a noise source.
