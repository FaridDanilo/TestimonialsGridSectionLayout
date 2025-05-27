body {
  font-family: 'Barlow Semi Condensed', sans-serif;
  background-color: hsl(210, 46%, 95%);
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  margin: 0;
  padding: 20px;
  box-sizing: border-box;
}

main {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(2, auto);
  gap: 20px;
  max-width: 1100px;
  width: 100%;
}

.testimonial {
  background-color: white;
  border-radius: 8px;
  padding: 30px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: column;
}

.testimonial-1 {
  background-color: hsl(263, 55%, 52%);
  color: hsl(0, 0%, 100%);
  grid-column: 1 / span 2;
  grid-row: 1;
  position: relative;
  z-index: 1;
}

.testimonial-2 {
  background-color: hsl(217, 19%, 35%);
  color: hsl(0, 0%, 100%);
  grid-column: 3 / span 1;
  grid-row: 1;
}

.testimonial-3 {
  background-color: hsl(0, 0%, 100%);
  color: hsl(217, 19%, 35%);
  grid-column: 1 / span 1;
  grid-row: 2;
}

.testimonial-4 {
  background-color: hsl(219, 29%, 14%);
  color: hsl(0, 0%, 100%);
  grid-column: 2 / span 2;
  grid-row: 2;
}

.testimonial-5 {
  background-color: hsl(0, 0%, 100%);
  color: hsl(217, 19%, 35%);
  grid-column: 4 / span 1;
  grid-row: 1 / span 2;
}

.testimonial img {
  border-radius: 50%;
  width: 40px;
  height: 40px;
  object-fit: cover;
  margin-right: 15px;
}

.testimonial-name {
  font-weight: 600;
  margin-bottom: 0;
  line-height: 1.2;
}

.testimonial-status {
  opacity: 0.5;
  font-size: 0.85em;
  margin-top: 5px;
}

.testimonial-summary {
  font-size: 1.2em;
  font-weight: 600;
  line-height: 1.4;
  margin: 15px 0;
}

.testimonial-quote {
  font-size: 0.9em;
  line-height: 1.6;
  opacity: 0.7;
}

@media (max-width: 1024px) {
  main {
    grid-template-columns: repeat(3, 1fr);
    grid-template-areas:
      "t1 t1 t2"
      "t3 t4 t4"
      "t5 t5 t5";
  }

  .testimonial-1 { grid-area: t1; }
  .testimonial-2 { grid-area: t2; }
  .testimonial-3 { grid-area: t3; }
  .testimonial-4 { grid-area: t4; }
  .testimonial-5 { grid-area: t5; }
}

@media (max-width: 768px) {
  main {
    grid-template-columns: repeat(2, 1fr);
    grid-template-areas:
      "t1 t1"
      "t2 t5"
      "t3 t4";
  }
}

@media (max-width: 600px) {
  main {
    grid-template-columns: 1fr;
    grid-template-areas:
      "t1"
      "t2"
      "t3"
      "t4"
      "t5";
  }
}

.attribution {
  font-size: 11px;
  text-align: center;
  margin-top: 20px;
  position: absolute;
  bottom: 10px;
  width: 100%;
}

.attribution a {
  color: hsl(228, 45%, 44%);
}