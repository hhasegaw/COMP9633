<template>
  <div>
    <div style="padding-bottom: 150px;">
      <div class="container">
        <div class="columns">
          <div v-for="card in cards" class="column col-4">
            <gbc-card v-bind="card"></gbc-card>
            <!-- <GbcCard v-bind="card" /> -->
            <!--
              <gbc-card
                v-bind:title="card.title"
                v-bind:subtitle="card.subtitle"
                v-bind:body="card.body"
                v-bind:imgSrc="card.imgSrc"
              ></gbc-card>
            -->
          </div>
        </div>
      </div>
    </div>

    <GbcHeading title="hello" another="test" />
    <gbc-heading title="goodbye"></gbc-heading>
    <gbc-button></gbc-button>
    <gbc-accordion title="Accordion 1"></gbc-accordion>
    <gbc-accordion title="Accordion 2"></gbc-accordion>
  </div>
</template>

<script>
import GbcHeading from "./components/heading";
import GbcButton from "./components/button";
import GbcAccordion from "./components/accordion";
import GbcCard from "./components/card";

export default {
  name: "App",
  components: {
    GbcHeading,
    GbcButton,
    GbcAccordion,
    GbcCard
  },
  data() {
    return {
      cards: [
        {
          title: "CN Tower",
          subtitle: "Best place ever",
          body: "The food is pretty bad but the view is great",
          imgSrc:
            "https://www.torontobusco.com/wp-content/uploads/2017/05/n-dd-600x400.jpg"
        },
        {
          title: "Niagara Falls CA",
          subtitle: "Second best",
          body: "The food is horrible but the view is decent",
          imgSrc:
            "https://media-cdn.tripadvisor.com/media/photo-s/0f/73/db/0a/niagara-falls-boat-tour.jpg"
        },
        {
          title: "Niagara Falls US",
          subtitle: "Second best",
          body: "The food is horrible but the view is decent",
          imgSrc:
            "https://media-cdn.tripadvisor.com/media/photo-s/0f/73/db/0a/niagara-falls-boat-tour.jpg"
        }
      ]
    };
  }
};
</script>
