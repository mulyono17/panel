@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Japanese&display=swap');

@layer mShadow, mGradientStroke;

html, body {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  margin: 0;
  box-sizing: border-box;
  font-family: "Noto Sans JP", sans-serif;
  font-optical-sizing: auto;
  font-style: normal;
  background-color: #000;
}

@layer mShadow {
	h1 {
		/* Text Fill GRadient */
		background-image: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(121,112,9,1) 43%, rgba(0,212,255,1) 100%);
		color: transparent;
		text-fill-color: transparent;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		-webkit-background-clip: text;

		font-size: 6rem;
		paint-order: stroke fill;
		text-shadow: 3px 3px 0px cyan, 5px 5px 0px darkcyan;
		transition: all 0.5s;
	}

	//h1::before {
		content: "*";
		font-size: 1em;
		position: relative;
		top: 0;
		z-index: -1;
		left: 0;
		transition: all 0.5s;
	}

	h1 {
		font-variation-settings: "wght" 100, "ital" 1, "rota" 20;
		//transform: translate(-20px, -20px);
		/* Multiple Shadows */
		text-shadow: 10px 10px 0px #07bcccdd,
			15px 15px 0px #e601c099,
			22px 22px 0px #e9019a88,
			31px 31px 0px #f4046877,
			42px 42px 10px #48289666;
		animation: hithere 1s ease infinite;
	}

	h1:hover {
		font-variation-settings: "wght" 100, "ital" 0, "rota" 0;
		text-shadow: 10px 10px 5px #07bccc44;
		/* Text Stroke */
		-webkit-text-stroke: 1px #fff;
		animation-play-state: paused;
	}
}

@keyframes hithere {
  30% { transform: scale(1.1); }
  40%, 60% { transform: rotate(-5deg) scale(1.1); }
  50% { transform: rotate(5deg) scale(1.1); }
  70% { transform: rotate(0deg) scale(1.1); }
  100% { transform: scale(1.0); }
}

.container {
  display: flex;
  gap: 2rem;
}

.column {
  font-size: 2rem;
  padding: 1rem;
  text-align: center;
}

/* Layer for text stroke */
@layer tStroke {
  .text-stroke {
    -webkit-text-stroke: 0.3px #fff;
    color: #000;
  }
}

/* Layer for text gradient fill */
@layer tGradient {
  .text-gradient {
    background-image: linear-gradient(90deg, rgba(2, 0, 36, 1) 0%, rgba(121, 112, 9, 1) 43%, rgba(0, 212, 255, 1) 100%);
    color: transparent;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    -webkit-background-clip: text;
  }
}

/* Layer for multiple shadows */
@layer tShadows {
  .text-shadows {
    text-shadow: 5px 5px 0px #07bcccdd,
                 6px 6px 0px #e601c099,
                 8px 8px 0px #e9019a88,
                 11px 11px 0px #f4046877,
                 15px 15px 10px #48289666;
  }
}
