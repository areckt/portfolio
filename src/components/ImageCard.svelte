<script>
  export let imgData;
</script>

<a href={imgData.link} target="_blank" rel="noopener noreferrer" class="d_card" style="--img-url: url({imgData.imgUrl})">
  <div class="content">
    <h2 class="heading">{imgData.title}</h2>
    <p class="data-content">{imgData.description}</p> 
  </div>
</a>

<style>
:root {
  --d: 700ms;
  --e: cubic-bezier(0.19, 1, 0.22, 1);
}

.d_card,
.content,
.heading,
.data-content {
  box-sizing: border-box;
}

.d_card {
  position: relative;
  display: flex;
  align-items: flex-end;
  overflow: hidden;
  padding: 1rem;
  width: 100%;
  aspect-ratio: 16/9;
  text-align: center;
  background-color: transparent;
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.1), 0 2px 2px rgba(0, 0, 0, 0.1),
    0 4px 4px rgba(0, 0, 0, 0.1), 0 8px 8px rgba(0, 0, 0, 0.1),
    0 16px 16px rgba(0, 0, 0, 0.1);
  border-radius: 15px;
  transition: box-shadow calc(var(--d) * 1.5) var(--e);
}
.d_card:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 110%;
  background-image: var(--img-url);
  background-size: cover;
  background-position: 50% 50%;
  transition: transform calc(var(--d) * 1.5) var(--e);
  pointer-events: none;
}
.d_card:after {
  content: "";
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 200%;
  pointer-events: none;
  background-image: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0) 0%,
    rgba(0, 0, 0, 0.009) 11.7%,
    rgba(0, 0, 0, 0.034) 22.1%,
    rgba(0, 0, 0, 0.072) 31.2%,
    rgba(0, 0, 0, 0.123) 39.4%,
    rgba(0, 0, 0, 0.182) 46.6%,
    rgba(0, 0, 0, 0.249) 53.1%,
    rgba(0, 0, 0, 0.32) 58.9%,
    rgba(0, 0, 0, 0.394) 64.3%,
    rgba(0, 0, 0, 0.468) 69.3%,
    rgba(0, 0, 0, 0.54) 74.1%,
    rgba(0, 0, 0, 0.607) 78.8%,
    rgba(0, 0, 0, 0.668) 83.6%,
    rgba(0, 0, 0, 0.721) 88.7%,
    rgba(0, 0, 0, 0.762) 94.1%,
    rgba(0, 0, 0, 0.79) 100%
  );
  transform: translateY(-50%);
  transition: transform calc(var(--d) * 2) var(--e);
}

.content {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  padding: 1rem;
  transition: transform var(--d) var(--e);
  z-index: 1;
}
.content > * + * {
  margin-top: 1rem;
}

.heading {
  font-size: 1.3rem;
  font-weight: bold;
  font-family: 'Poppins';
  line-height: 1.2;
}

.data-content {
  font-size: 1.125rem;
  line-height: 1.35;
}

@media (hover: hover) and (min-width: 600px) {
  .d_card:after {
    transform: translateY(0);
  }

  .content {
    transform: translateY(calc(100% - 4.5rem));
    transition: transform var(--d) var(--e);
  }
  .content > *:not(.heading) {
    opacity: 0.5;
    transform: translateY(2rem);
    transition: transform var(--d) var(--e), opacity var(--d) var(--e);
  }

  .d_card:hover,
  .d_card:focus-within {
    box-shadow: 0px 1px 4px 1px rgb(125, 211, 252),
    0 1px 1px rgba(0, 0, 0, 0.1), 0 2px 2px rgba(0, 0, 0, 0.1),
    0 4px 4px rgba(0, 0, 0, 0.1), 0 8px 8px rgba(0, 0, 0, 0.1),
    0 16px 16px rgba(0, 0, 0, 0.1),
    0px 14px 55px rgba(56, 189, 248, 0.45);
  }
  .d_card:hover:before,
  .d_card:focus-within:before {
    transform: translateY(-4%);
  }
  .d_card:hover:after,
  .d_card:focus-within:after {
    transform: translateY(-50%);
  }
  .d_card:hover .content,
  .d_card:focus-within .content {
    transform: translateY(-1rem);
  }
  .d_card:hover .content > *:not(.heading),
  .d_card:focus-within .content > *:not(.heading) {
    opacity: 1;
    transform: translateY(0);
    transition-delay: calc(var(--d) / 8);
  }
}

</style>