<script setup>
import { ref, computed, onMounted } from "vue";
import ListItem from "./ListItem.vue";

const storageItems = ref([]);

const setToStorage = (items) => {
  localStorage.setItem("list-items", JSON.stringify(items));
};

const getFromStorage = () => {
  const stored = localStorage.getItem("list-items");
};

const initListItems = () => {
  if (storageItems.value.length === 0) {
    const listItems = [
      { title: "Make a Todo App", checked: false },
      { title: "Buy Flower", checked: false },
      { title: "Learn a new Technology", checked: true },
      { title: "Feed the Fish", checked: true },
      { title: "Learn Vue", checked: false },
    ];
    setToStorage(listItems);
    storageItems.value = listItems;
  }
};

const sortedList = computed(() => {
  return [...storageItems.value].sort(
    (a, b) => (a.checked ? 1 : 0) - (b.checked ? 1 : 0)
  );
});

const updateItem = (item) => {
  const index = storageItems.value.findIndex((i) => i.title === item.title);
  storageItems.value[index].checked = item.checked;
  setToStorage(storageItems.value);
};
const findItemInList = (title) => {
  return storageItems.value.find((i) => i.title === title);
};
</script>

<template></template>

<style scoped></style>
