# Rendering Lists

To display list of items in React, you can use JavaScript Array methods like `map` and `filter`.

```jsx
export const students = [
  "Mohamed Ali",
  "Mustafe Hassan",
  "Mohammad Abdus Salam",
  "Maryam Mohamoud",
  "Hamda Warsame",
  "Mohamed Abdi",
];
```

we can use `map` to render list of items:

```jsx
<ul>
  {students.map((student, index) => (
    <li key={index}>{student}</li>
  ))}
</ul>
```

Note: `key` is used to identify each item in the list.

You need to give each array item a unique key — a string or a number that uniquely identifies it among other items in that array:

## Filtering arrays of items

you can use `filter` to filter items in the list: and display only those items that match the condition:

```jsx
export const students = [
  {
    id: 0,
    name: "Mohamed Ali",
    track: "Full Stack",
    skills: ["HTML", "CSS", "JavaScript", "PHP"],
    photo: "mohamed.png",
  },
  {
    id: 1,
    name: "Mustafe Hassan",
    track: "Front End",
    skills: ["HTML", "CSS", "JavaScript", "Python", "Flutter"],
    photo: "mustafe.png",
  },
  {
    id: 2,
    name: "Mohammad Abdus Salam",
    track: "Full Stack",
    skills: ["HTML", "CSS", "JavaScript", "PHP"],
    photo: "salam.png",
  },
  {
    id: 3,
    name: "Maryam Mohamoud",
    track: "Full Stack",
    skills: ["HTML", "CSS", "JavaScript", "Java", "jQuery"],
    photo: "maryam.jpg",
  },
  {
    id: 4,
    name: "Hamda Warsame",
    track: "Front End",
    skills: ["HTML", "CSS", "JavaScript"],
    photo: "hamda.png",
  },
```

display only full stack students

```jsx
const fullStackStudents = students.filter(
  (student) => student.track === "Full Stack"
);
<ul>{fullStackStudents}</ul>;
```

this will display only full stack students in the list:
