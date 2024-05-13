<!-- App.svelte -->
<script>
	let name = 'User';
	let major = 'Computer Engineering Undergraduate at McMaster University';
  
	const updateButton = () => {
		major = 'Masters Electrical Engineering & Computer Science Student at UCal Berkeley';
	};
  </script>
  
  <main>
	  <div class="stars"></div>
	  <div class="container">
		  <h1>Hello {name}!</h1>
		  <p>My name is Sameer Suleman, I'm currently a {major}</p>
		  <button on:click={updateButton}>Graduate</button>
	  </div>
  </main>
  
  <style>
	  main {
		  text-align: center;
		  padding: 1em;
		  max-width: 240px;
		  margin: 0 auto;
		  position: relative;
		  z-index: 1;
	  }
  
	  h1 {
		  color: #ff3e00;
		  text-transform: uppercase;
		  font-size: 4em;
		  font-weight: 100;
	  }
  
	  .stars {
		  position: fixed;
		  top: 0;
		  left: 0;
		  width: 100%;
		  height: 100%;
		  pointer-events: none;
		  background: url('https://www.transparenttextures.com/patterns/black-linen.png'), radial-gradient(white 2%, transparent 2%);
		  background-size: cover;
		  z-index: 0;
		  animation: stars 50s infinite linear;
	  }
  
	  @keyframes stars {
		  0% {
			  background-position: 0 0, 0 0, 0 0;
		  }
		  50% {
			  background-position: 500px 500px, 500px 500px, 500px 500px;
		  }
		  100% {
			  background-position: 0 0, 0 0, 0 0;
		  }
	  }
  
	  @media (min-width: 640px) {
		  main {
			  max-width: none;
		  }
	  }
  </style>
  