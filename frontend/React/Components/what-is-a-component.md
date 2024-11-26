# TIL: What is a component and how does it work
_25-11-2024_

- 👉 [Components by Gentleman Programming 📺]()


A `component` is:

- A minimum logical unit 🟧
- A function that gets executed ⚙️ and its result is rendered.
- It should only contain the logic 📐 it belongs to. _(single responsabilty principle vibes? 🤔)_



![image](https://github.com/user-attachments/assets/60e239f4-c999-479c-9fcc-1de316ab4392)

>[!NOTE]
> Each component always returns HTML-like code (JSX).

![image](https://github.com/user-attachments/assets/1c3a436f-d045-47b3-ba30-6fb510697ad5)


For that reason, you can add millions of dashboards if you wish 🤡. 
Each of them is a different instance, __since the same function is executed multiple times.__

---
Your job will be to minimize the number of these renderings
<img src="https://github.com/user-attachments/assets/8f2cc658-f131-4fef-b9e8-c54792ce91cf" alt="uncle-sam-pointing-finger" height="400"/>
