<template>
  <RouterLink
    v-if="noEditCardOpen()"
    class="edit-button"
    :to="{
      name: 'Edit Profile',
      query: {
        section: sectionId,
      },
    }"
  >
    <Icon id="pencil" :width="20" :height="20"></Icon>
    <span class="visually-hidden">Edit {{ section }}</span>
  </RouterLink>
  <button type="button" v-else class="edit-button" v-on:click="saveOrDiscard">
    <Icon id="pencil" :width="20" :height="20"></Icon>
    <span class="visually-hidden">Edit {{ section }}</span>
  </button>
</template>

<script>
import Icon from '@/components/ui/Icon.vue';
import contentLookup from '@/assets/js/content-lookup';

export default {
  name: 'EditButton',
  props: {
    section: String,
    sectionId: String,
  },
  components: {
    Icon,
  },
  methods: {
    noEditCardOpen() {
      return this.$route.name !== 'Edit Profile' || !this.$route.query.section;
    },
    saveOrDiscard() {
      const section = contentLookup[this.$route.query.section];
      const content = `Please discard or save your changes in the '${section}' section first.`;
      this.$root.$emit('toast', { content });
    },
  },
};
</script>

<style>
.edit-button {
  border: none;
  background: none;
  color: var(--black);
}
.edit-button:hover {
  color: var(--blue-60);
}
.profile__section-header .edit-button {
  position: absolute;
  top: 1.5em;
  right: 1.5em;
}
.profile__intro .edit-button {
  position: absolute;
  top: 1em;
  right: 0;
}
</style>
