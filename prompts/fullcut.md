# fullcut prompts


## wall

**full cut, the achievements wall after his death, 1962**

length 16.0 · credits 0 · takes 1 · verdict keep

```
A high-prestige, cinematic 16:9 horizontal still, a long wall inside a deep, quiet, high-ceilinged panelled study, lit flatly and coolly by grey overcast daylight falling from a tall window out of frame to the left. Deep polished dark teak panelling runs unbroken across the whole wall with visible natural wood grain. Hanging on it in one straight horizontal line at shoulder height are six plain dark wooden picture frames, evenly spaced, each holding a black and white photograph, except the last. From left to right: a long two-storey pale plastered hospital building with a deep shaded verandah; an empty lecture theatre of curved dark wooden benches rising steeply in tiers; a wide concrete barrage spanning a broad river; a heavy industrial works with tall chimneys; a newly built planned township seen from high above, with wide straight avenues on a regular grid and open green squares. The sixth frame at the right end is larger than the other five and holds a drawn architectural plan of a town, a grid of streets and open green squares in fine black line on pale cream paper. Below the wall stands a dark teak desk, and on it a green-shaded brass banker's lamp stands dark and unlit. The frames are plain and bare, with nothing hung, fixed or mounted beneath any of them, and the panelling between and around them is bare polished wood. No people are present in the room, and no people are visible in any of the photographs. No writing, no lettering and no readable text of any kind appears anywhere in the image, on any photograph, on the plan, or on the wall. Colour is rich, fully saturated and varied across the frame: dark red-brown teak, pale cream paper, cool photographic grey, aged brass green, and cool overcast daylight grey. Clean, crisp, contemporary finish.
```

**What happened**

> FREE. A still with a lateral pan rendered locally by ffmpeg, the same route as ep13 beat 2's push-in.
> 
> GENERATED 16:9 AND PANNED TO 9:16, which is the point. A lateral move across six pictures needs a wide source. Panning a 864x1536 window across a 2752x1536 still keeps every frame large, where six frames inside a 9:16 generation would each have been too small to read. Travel is 1888px.
> 
> THE MOVE EASES OUT. x = 1888 * smoothstep(t/16), so it arrives on the plan and settles rather than stopping dead on the last frame. A pan that halts abruptly is what makes these read as a slideshow. Command in docs/ASSEMBLY.md.
> 
> 16 SECONDS ON CHAND'S EYE. 10 was rendered first and he called it too fast; 14 and 16 were rendered for comparison and he took 16, which also matches the narration's 16.77s.
> 
> THE SAME WALL AS ep13 BEAT 2, LAMP OUT. Beat 2 is three pictures lit warm by the green-shaded banker's lamp at night while he is alive and working. This is the same panelled wall seen wider in flat cold daylight with the lamp dark, and six frames visible instead of three. Keeping the object and changing its state is the ep06 beat 8 move, and it ties the two together harder than a new room would. The viewer is not shown a new wall, they are shown the rest of a wall they have already stood in front of.
> 
> NOTHING WAS ATTACHED. Prose carried the room, as it did throughout ep12 and ep13. Attaching beat 2's night frame to a daylight shot is the ep06 beat 8 trap, where the model renders the change instead of the destination.
> 
> THE ORDER ENDS ON KALYANI so the city hands over to Sushil's 1975 beat: hospital, lecture theatre, barrage, steelworks, township, then the plan. Medicine, then engineering, then cities, then the plan.
> 
> THE PLAN WAS CHECKED AT FULL RESOLUTION and carries no lettering, no title block and no legend. It is the frame the move rests on, so it was the one worth checking.
