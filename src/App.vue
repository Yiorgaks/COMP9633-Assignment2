<template>
  <div>
    <div style="padding-bottom: 150px;">
      <h3>Assignment #1</h3>
      <ul>
        <li></li>
        <li>Build a table Component</li>
        <li>
          Use the HTML from
          <a
            href="https://picturepan2.github.io/spectre/elements/tables.html"
            target="_blank"
            >Spectre</a
          >
          and follow the same steps we used in class to make a Component
        </li>
        <li>Ensure that the table renders with the correct data first</li>
        <li>Use the 'cards' data to render rows inside the table</li>
        <li>
          Once your table renders, try to split it up into further components
        </li>
        <ul>
          <li>Table component will have inside a TableHead Component</li>
          <li>Table component will have inside a TableBody Component</li>
          <li>TableHead component will have inside a TableRow Component</li>
          <li>TableBody component will have inside a TableRow Component</li>
        </ul>
        <li>
          Send complete (or as far as you can get) assignment to
          js.alex.gbc@gmail.com before next class (Nov 29)
        </li>
        <li>
          Send either the codesandbox link or a link to your github page of the
          assignment
        </li>
      </ul>

      <gbc-table v-bind:rows="cards"></gbc-table>

      <div style="height: 50px;"></div>

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
import GbcTable from "./components/table";

export default {
  name: "App",
  components: {
    GbcHeading,
    GbcButton,
    GbcAccordion,
    GbcCard,
    GbcTable
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
