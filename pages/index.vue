<template>
  <div>
    <Header />
    <Home />
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat+Alternates:wght@300;400;700;900&display=swap");
*,
*::before,
*::after {
  box-sizing: inherit;
  margin: 0;
}
html {
  box-sizing: border-box;
  scroll-behavior: smooth;
  min-width: 320px;
  background: black;
  color: white;
}
body {
  font-family: "Montserrat Alternates", sans-serif;
  font-size: 14px;
  color: white;
}
img {
  object-fit: cover;
}
a {
  cursor: pointer;
  text-decoration: none;
  color: white;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-size: 1em;
  font-weight: 400;
}
button,
button::before,
button::after {
  cursor: pointer;
  font-family: "Montserrat Alternates", sans-serif;
  border: none;
  background: transparent;
  color: white;
  font-size: 1em;
  font-weight: 400;
}
input,
input::before,
input::after,
textarea,
textarea::before,
textarea::after {
  font-family: "Montserrat Alternates", sans-serif;
  border: none;
  resize: none;
  color: white;
  font-size: 1em;
  font-weight: 400;
}
ul,
ul::before,
ul::after,
li,
li::before,
li::after {
  display: flex;
  justify-content: space-between;
  align-items: center;
  list-style-type: none;
  padding: 0;
}
</style>
