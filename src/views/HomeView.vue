<script setup lang="ts">
import BenefitsCard from "../components/BenefitsCard.vue"

const benefits = [
  {
    id: 1,
    title: "Reduce monthly payment",
    description:
      "Reduce your monthly payment substantially by refinancing your loan balance over a 30-year period",
    img: "/src/assets/monthly-payment.png",
  },
  {
    id: 2,
    title: "Pay off your home loan",
    description:
      "In addition to paying off your loan sooner, refinancing into a shorter term loan will also result in significant interest cost savings.",
    img: "/src/assets/pay-off.png",
  },
  {
    id: 3,
    title: "Build home equity faster",
    description:
      "Your monthly payments go more toward building your home equity if your lower your rate and/or decrease the length of your loan.",
    img: "/src/assets/build-home.png",
  },
]

const details = [
  {
    id: 1,
    title: "Best Rate",
    description:
      "To discover the best rate for you, we sort through hundreds of loan products and programs from different lenders.",
  },
  {
    id: 2,
    title: "Transparent",
    description:
      "To maximize your savings, we use our in-depth product expertise and industry experience.",
  },
  {
    id: 3,
    title: "Fast",
    description:
      "We use artificial intelligence (AI) technology to monitor and manage our loan pipeline and hasten your loan completion.",
  },
  {
    id: 4,
    title: "Experienced",
    description:
      "We use the newest technological technologies to give you a flawless and easy client experience.",
  },
  {
    id: 5,
    title: "Easy",
    description:
      "To give you a flawless and easy client experience, we use the most recent technological tools.",
  },
  {
    id: 6,
    title: "Efficient",
    description:
      "We are trained to minimize the back and forth by not asking you for the same documents multiple times.",
  },
]
</script>

<template>
  <div>
    <header
      class="bg-secondary px-6 py-8 md:py-20 rounded-[36px] flex flex-col-reverse gap-y-4 mb-10 gap-x-20 md:gap-y-0 md:flex-row md:items-center lg:gap-x-28 md:mb-20 md:w-[110%] md:-ml-[5%]"
    >
      <img
        class="md:w-[50%] lg:max-w-none"
        src="../assets/home-vue.png"
        alt="header"
        width="548"
        height="455"
      />
      <div class="flex flex-col gap-y-4 md:gap-y-8 md:max-w-[35%]">
        <span class="text-primary font-semibold text-lg"
          >Rate & Term Refinance</span
        >
        <h1 class="text-3xl md:text-5xl font-semibold">
          Quickly Increase Your Home Equity
        </h1>
        <p class="hidden md:block text-base text-slate-500">
          By refinancing your mortgage through a rate and term refinance, you
          have the opportunity to lower your interest rate and shorten the term
          of your loan, which can result in making more payments towards the
          principal. This can help you save money on interest and pay off your
          mortgage faster, putting you in a better financial position.
        </p>
        <span class="border border-primary w-fit rounded-lg">
          <button
            class="py-2 px-10 w-fit bg-primary ring-1 ring-primary text-semibold text-white rounded-lg transition-all hover:-translate-x-1 hover:-translate-y-1"
          >
            Get Started
          </button>
        </span>
      </div>
    </header>
    <main class="flex flex-col md:gap-y-8 mb-20">
      <div
        class="flex flex-col gap-y-4 md:flex-row items-baseline justify-between mb-10 md:mb-20"
      >
        <h2 class="text-3xl md:text-5xl font-semibold md:max-w-[30%]">
          Benefits of rate & term refinance
        </h2>
        <p class="text-base text-slate-500 md:max-w-[45%]">
          If you currently have a mortgage and you are looking to change the
          terms of that mortgage without borrowing more money. then rate and
          term refinance may be a good option for you.
        </p>
      </div>
      <div
        class="grid gap-y-4 md:grid-cols-3 items-center justify-between gap-x-4 lg:gap-x-12 min-w-[300px]"
      >
        <BenefitsCard
          class="h-full"
          v-for="benefit in benefits"
          :key="benefit.id"
          :title="benefit.title"
          :description="benefit.description"
          :img="benefit.img"
        />
      </div>
    </main>
    <footer
      class="bg-secondary px-6 py-8 md:px-12 md:py-20 rounded-[36px] grid md:grid-cols-2 md:gap-x-24 md:mb-20 md:w-[110%] md:-ml-[5%]"
    >
      <div class="rounded-3xl h-full bg-primary/90 hidden md:block"></div>
      <div>
        <h3 class="text-3xl md:text-5xl font-semibold mb-12">
          Relax, You are <br />
          in Good Hands
        </h3>
        <ul class="grid md:grid-cols-2 gap-10">
          <li v-for="detail in details" :key="detail.id">
            <h4 class="text-2xl font-semibold mb-4">{{ detail.title }}</h4>
            <p class="text-slate-500">{{ detail.description }}</p>
          </li>
        </ul>
      </div>
    </footer>
  </div>
</template>
