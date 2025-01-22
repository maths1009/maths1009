![header](https://gitlab.com/maths1009/maths1009/-/raw/main/header.gif?ref_type=heads)

```jsx
import { useState } from "react";

const useHobbies = () => {
  return [
    "Football",
    "Watching marvels",
    "Going out with friends",
    "Being up all Night chasing that ONE BUG...",
  ];
};

export const Readme = () => {
  const [user, setUser] = useState("Brangeon Mathis");
  const [currentWork, setCurrentWork] = useState("Writing code...");
  const hobbies = useHobbies();

  const city = "Angers, France";

  return (
    <div>
      <h1>👋 Hey there! I'm {user}</h1>
      <p>I'm currently {currentWork}.</p>
      <h2>🌆 Location</h2>
      <p>I currently live in {city}.</p>
      <ul>
        {hobbies.map((hobby, index) => (
          /*don't forget key on map :)*/
          <li key={index}>{hobby}</li>
        ))}
      </ul>
    </div>
  );
};
```
