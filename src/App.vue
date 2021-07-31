<template>
  <div class="vehicles">
    <section class="vehicle">
      <img class="section-image" src="/images/icon-sedans.svg" alt="Icon showing a sedans car"/>
      <h2 class="section-title">SEDANS</h2>
      <p class="section-content">Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city or on your next road trip.</p>
      <button class="section-button">Learn More</button>
    </section>
    <section class="vehicle">
      <img class="section-image" src="/images/icon-suvs.svg" alt="Icon showing a suvs car"/>
      <h2 class="section-title">SUVS</h2>
      <p class="section-content">Take an SUV for its spacious interior, power, and versatility. Perfect for your next family vacation and off-road adventures.</p>
      <button class="section-button">Learn More</button>
    </section>
    <section class="vehicle">
      <img class="section-image" src="/images/icon-luxury.svg" alt="Icon showing a luxury car"/>
      <h2 class="section-title">LUXURY</h2>
      <p class="section-content">Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury rental and arrive in style.</p>
      <button class="section-button">Learn More</button>
    </section>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
@import url('https://fonts.google.com/specimen/Lexend+Deca');
@import url('https://fonts.google.com/specimen/Big+Shoulders+Display');
:root {
  --primary-bright-orange: hsl(31, 77%, 52%);
  --primary-dark-cyan: hsl(184, 100%, 22%);
  --primary-very-dark-cyan: hsl(179, 100%, 13%);
  --neutral-transparent-white: hsla(0, 0%, 100%, 0.75); /*(paragraphs)*/
  --neutral-very-light-gray: hsl(0, 0%, 95%); /*(background, headings, buttons)*/
}

body {
  margin: 0;
  padding: 0;
  font-family: 'Lexend Deca', sans-serif;
  font-weight: 400;
  font-size: 1.5rem;
}

#app {
  font-family: 'Lexend Deca', sans-serif;
  height: 100%;
  width: 100vw;
  background-color: var(--neutral-very-light-gray);
  display: flex;
  flex-direction: column;
  align-content: center;
}

.vehicles {
  margin: 50px 0 50px 0;
  display: flex;
  align-self: center;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  height: 100%;
  width: 80%;
}

.vehicles > .vehicle:first-child {
  background-color: var(--primary-bright-orange);
  border-radius: 3% 3% 0 0;
}

.vehicles > .vehicle {
  background-color: var(--primary-dark-cyan);
  padding: 3rem;
}

.vehicles > .vehicle:last-child {
  background-color: var(--primary-very-dark-cyan);
  border-radius: 0 0 3% 3%;
}

.vehicle .section-title {
  font-family: 'Big Shoulders Display', sans-serif;
  font-weight: 700;
  color: var(--neutral-very-light-gray);
  font-size: 1.4rem;
}

.vehicle .section-content {
  color: var(--neutral-transparent-white);
  font-size: 1rem;
}

.vehicle:first-child .section-button {
  color: var(--primary-bright-orange);
}

.vehicle:first-child .section-button:hover {
  background-color: var(--primary-bright-orange);
  color: var(--neutral-very-light-gray);
}

.vehicle .section-button {
  background-color: var(--neutral-very-light-gray);
  padding: 10px 20px;
  border-radius: 50px;
  border: 0;
  font-size: 1.1rem;
  color: var(--primary-dark-cyan);
}

.vehicle .section-button:hover {
  background-color: var(--primary-dark-cyan);
  color: var(--neutral-very-light-gray);
  border: 1px solid var(--neutral-very-light-gray);
  cursor: pointer;
}

.vehicle:last-child .section-button {
  color: var(--primary-very-dark-cyan);
}

.vehicle:last-child .section-button:hover {
  background-color: var(--primary-very-dark-cyan);
  color: var(--neutral-very-light-gray);
}

@media (min-width: 960px) {
  #app {
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .vehicles {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-content: center;
    height: 80%;
    width: 80%;
  }

  .vehicles > .vehicle:first-child {
    border-radius: 3% 0 0 3%;
  }

  .vehicles > .vehicle {
    padding: 2.5rem;
  }

  .vehicles > .vehicle:last-child {
    border-radius: 0 3% 3% 0;
  }

  .vehicle .section-title {
    font-size: revert;
  }

  .vehicle .section-content {
    font-size: 1.2rem;
  }

  .vehicle .section-button {
    margin-top: 20vh;
    font-size: 1.3rem;
  }
}
</style>
