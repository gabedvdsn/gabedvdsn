## Hi there 👋

##### *I'm currently working on*
>### Research study utilizing VR in Unity

**The Research**

My current project is a research project utilizing VR within the Unity game engine for a study titled "Mitigating the Risk of Fire Evacuations Using Virtual Reality and Artificial Intelligence." 
My partners, Nikhil Ahuja and Caden Goodwin, are also contributors to this project. 

Our research question pertains to how natural human instinct during an active fire evacuation aligns with fire evacuation protocol. To accomplish this, we created multiple simulation scenes within Unity and imported the necessary building assets and VR packages. We utilized a MetaQuest 3 Headset for this project.

**My Role**

My role in the project was to script the game logic.

1. Fire & Fire Propagation
2. Environmental Variables
3. The Player
4. The Manager

>**1. Fire & Fire Propagation**

We needed fire, and we needed it to spread. And we also needed it to follow realistic patterns of fire behavior. Well, at least to a degree (see **Simulation Limitations**)

I developed a Fire Node script, which tracked its temperature and health (fuel/durability). FireNodes would be assigned a Material Type, such as wood, metal, or plastic. Combusted Fire Nodes would emit heat to neighboring nodes. When the temperature got high enough, it would combust. And when its health gets too low... then what?

Next I developed a Fire Anchor script, which corresponded to something, like an object, in the simulation. It tracks the Fire Nodes within its sub-hierarchy. When nodes deplete their health, the Fire Anchor tells them to either continue burning or extinguish.

I created a static class called FirePropagation to handle all Fire Node initialization. Computing Fire Node variables each frame would be rudely inefficient. This class held information regarding combustion temperatures, maximum temperatures, and heating rates for each Material Type. 

<!--
**gabedvdsn/gabedvdsn** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
