# StarRating-file

A reusable Star Rating Component built with React that allows users to rate items using interactive stars.
The component is customizable and can be reused in different projects.

## 🚀Features

- Interactive star rating system
- Hover preview before selecting a rating
- Customizable number of stars
- Custom colors and sizes
- Optional rating messages (e.g., Terrible → Great)
- Default rating support
- Reusable component design
- Callback function to pass the selected rating to parent components

## 🛠 Technologies Used

- React (Hooks)
- JavaScript (ES6)
- PropTypes for type checking
- SVG icons for stars

## 📦 Component Props

- Prop	Type	Description
- maxRating	number	Maximum number of stars
- color	string	Color of the stars
- size	number	Size of the stars
- className	string	Custom CSS class
- messages	array	Custom messages for each rating
- defaultRating	number	Default selected rating
- onSetRating	function	Callback function returning selected rating

## 💻 Example Usage
<StarRating
  maxRating={5}
  size={24}
  color="blue"
  messages={["Terrible", "Bad", "OK", "Good", "Great"]}
/>

Example with state handling:

function Test() {
  const [movieRating, setMovieRating] = useState(0);

  return (
    <div>
      <StarRating
        maxRating={10}
        size={24}
        color="red"
        onSetRating={setMovieRating}
      />
      <p>This movie was rated {movieRating} stars</p>
    </div>
  );
}

## 🧠 How It Works

- The component uses React state to manage the selected rating and the temporary hover rating.
- rating stores the selected value.
- tempRating stores the hover preview.

When the user hovers over a star, the component shows a preview rating.
When the user clicks a star, the selected rating is saved and optionally sent to the parent component using the onSetRating callback.

## 🎯 Learning Concepts Used

- React Hooks (useState)
- Component Reusability
- Props and PropTypes validation
- Event Handling
- Conditional Rendering
- Dynamic UI Rendering


Author: 
[Haneen Abdelhaleem | https://www.linkedin.com/in/haneen-abdulhaleem20306/]
