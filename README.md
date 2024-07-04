Note. When I say reload your game I mean close the whole application and then reopen it and open a world. Doing this refreshes the shader, if you don't close your game then it won't refresh.

- Colored Artificial Light. Can be changed by going to nodes_shader/opengl_vertex.glsl and finding the part near the beginning of the file that has #define. whichever colored light you want. remove the // on that color and add // to the front of the previous color so that the file will ignore the old definition. Warm color by default.

<img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/Colored_Artificial_Light.png" />

- Same type of shader that affects the above also affects mobs. Same instructions as above, just go into object_shader
<img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/Mobs_In_Artificial_Light.png" />

 - Shader that adds colored natural light at dawn and dusk. Can be changed by going to nodes_shader/opengl_fragment.glsl and looking for the area that says #define TINTED_SUNLIGHT to disable tinted sunlight simply put // in front of #define. Reload your game and it should have the changes.
<img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/Colored_Lighting_At_Sunrise.png" />

- Same type of shader that affects the above also affect mobs. Same instructions as above, just go into object_shader
 <img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/Mobs_In_Tinted_Sunlight.png" />

 - Same shader that affects the above, is also used to make the following colored reflections. To disable the reflections however. Go to nodes_shader/opengl_fragment.glsl and look for the area that says #define LIQUID_REFLECTIONS and put // in front of the #define. Reload your game and it should have the changes.
<img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/Colored_Moon_Reflection.png" />
<img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/Colored_Sun_Reflection.png" />

- and yet again the same shader as above also makes the minimap change colors based on time. It can be disabled by going to minimap_shader/opengl_fragment.glsl and looking for #define TINTED_SUNLIGHT . The fut // in front of the #define. This will disable it.

<img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/COLORED_MINIMAP.png" />

- Stars that are meant to resemble fireworks. You can enable them by going to the stars_shader folder. Then to the opengl_fragment.glsl file then finding //FIREWORKS and removing the // . They are disabled by default.
<img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/Firework_Stars.png" />

- Shader that makes foliage almost translucent by allowing sunlight to go through it. To disable it, go to nodes_shader/opengl_fragment.glsl and look for the area that says #define TRANSLUCENT_FOLIAGE then put // in front of it. Reload your game and it will be disabled.
<img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/TRANSLUCENT_FOLIAGE.png" />

- Shader that makes foliage the way you see above also makes water translucent.
<img src="https://raw.githubusercontent.com/DragonWrangler1/minetest-5.8.0-shaderpack/main/TRANSLUCENT_LIQUID.png" />





This repo was largely based off of https://github.com/minetest/minetest/pull/14610
