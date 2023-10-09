<template>
  <q-page class="">
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">
        <q-input
          class="new-x"
          bottom-slots
          v-model="newXContent"
          placeholder="What's happening"
          counter
          maxlength="280"
          autogrow
        >
          <template v-slot:before>
            <q-avatar sixe="xl">
              <img src="https://cdn.quasar.dev/img/avatar5.jpg" />
            </q-avatar>
          </template>
        </q-input>
      </div>
      <div class="col col-shrink">
        <q-btn
          class="q-mb-lg"
          unelevated
          no-caps
          :disable="!newXContent"
          rounded
          color="primary"
          label="Send"
        />
      </div>
    </div>

    <q-separator class="divider" size="10px" color="grey-2" />

    <q-list class="">
      <q-item class="q-py-md">
        <q-item-section avatar top>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/avatar2.jpg" />
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitle1"
            ><strong>Guru</strong
            ><span class="text-grey-7 q-px-sm"
              >@Guru_worldwide</span
            ></q-item-label
          >
          <q-item-label class="x-content text-body1">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas
            aliquid praesentium deserunt neque quos quidem est iste assumenda,
            eius quasi nam sed iusto eligendi omnis molestias molestiae.
            voluptates aspernatur voluptatibus!
          </q-item-label>
          <div class="row justify-between q-mt-sm x-icons">
            <q-btn color="grey" icon="far fa-comment" size="sm" flat round />
            <q-btn color="grey" icon="fas fa-retweet" size="sm" flat round />
            <q-btn color="grey" icon="far fa-heart" size="sm" flat round />
            <q-btn color="grey" icon="fas fa-trash" size="sm" flat round />
          </div>
        </q-item-section>

        <q-item-section side top> 1 min ago </q-item-section>
      </q-item>
    </q-list>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageHome",
  data() {
    return {
      newXContent: "",
      xtweet: [
        {
          content:
            "ipsum dolor sit amet consectetur adipisicing elit. Qua aliquid praesentium deserunt neque quos quidem est iste assumenda, eius quasi nam sed iusto eligendi omnis molestias molestiae. voluptates aspernatur voluptatibus",
          date: 1611653238221,
          content:
            "ipsum dolor sit amet consectetur adipisicing elit. Qua aliquid praesentium deserunt neque quos quidem est iste assumenda, eius quasi nam sed iusto eligendi omnis molestias molestiae. voluptates aspernatur voluptatibus",
          date: 1611653238221,
          content:
            "ipsum dolor sit amet consectetur adipisicing elit. Qua aliquid praesentium deserunt neque quos quidem est iste assumenda, eius quasi nam sed iusto eligendi omnis molestias molestiae. voluptates aspernatur voluptatibus",
          date: 1611653238221,
        },
      ],
    };
  },
});
</script>

<style lang="sass">
.new-x
 textarea
  font-size: 19px
  line-height: 1.4 !important

.divider
  border-top: 1px solid
  border-bottom: 1px solid
  border-color: $grey-4

.x-content
  white-space: pre-line

.x-icons
  margin-left: -5px
</style>
