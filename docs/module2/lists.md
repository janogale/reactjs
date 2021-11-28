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
