![header](./header.gif)

```jsx
import { useState } from "react";

const useHobbies = (): string[] => {
  return [
    "Football",
    "Watching marvels",
    "Going out with friends",
    "Being up all Night chasing that ONE BUG...",
  ];
};

interface ReadmeProps {}

export const Readme: React.FC<ReadmeProps> = () => {
  const [user, setUser] = useState < string > "Brangeon Mathis";
  const [currentWork, setCurrentWork] = useState < string > "Writing code...";
  const hobbies: string[] = useHobbies();

  const city: string = "Angers, France";

  return (
    <div>
      <h1>👋 Hey there! I'm {user}</h1>
      <p>I'm currently {currentWork}.</p>
      <h2>🌆 Location</h2>
      <p>I currently live in {city}.</p>
      <ul>
        {hobbies.map((hobby: string, index: number) => (
          /*don't forget key on map :)*/
          <li key={index}>{hobby}</li>
        ))}
      </ul>
    </div>
  );
};
```
