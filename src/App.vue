<template>
  <div v-if="isWebF">
    <Routes>
      <Route path="/" :element="HomePage" title="Home" />
      <Route path="/button" :element="ButtonPage" title="Button" />
      <Route path="/switch" :element="SwitchPage" title="Switch" />
      <Route path="/input" :element="InputPage" title="Input" />
      <Route path="/icon" :element="IconPage" title="Icon" />
      <Route path="/search_input" :element="SearchInputPage" title="SearchInput" />
      <Route path="/textarea" :element="TextareaPage" title="Textarea" />
      <Route path="/segmented_tab" :element="SegmentedTabPage" title="Segmented Tab" />
      <Route path="/alert" :element="AlertPage" title="Alert" />
      <Route path="/date_picker" :element="DatePickerPage" title="Date Picker" />
      <Route path="/loading" :element="LoadingPage" title="Loading" />
      <Route path="/modal_popup" :element="ModalPopupPage" title="Modal Popup" />
      <Route path="/picker" :element="PickerPage" title="Picker" />
      <Route path="/slider" :element="SliderPage" title="Slider" />
      <Route path="/context_menu" :element="ContextMenuPage" title="Context Menu" />
      <Route path="/checkbox" :element="CheckboxPage" title="Checkbox" />
      <Route path="/radio" :element="RadioPage" title="Radio" />
      <Route path="/timer_picker" :element="TimerPickerPage" title="Timer Picker" />
      <Route path="/action_sheet" :element="ActionSheetPage" title="Action Sheet" />
      <Route path="/form_row" :element="FormRowPage" title="Form Row" />
      <Route path="/form_section" :element="FormSectionPage" title="Form Section" />
      <Route path="/list_tile" :element="ListTilePage" title="List Tile" />
      <Route path="/list_section" :element="ListSectionPage" title="List Section" />
      <Route path="/tab_bar" :element="TabBarPage" title="Tab Bar" />
    </Routes>
  </div>
  <div v-else>
    <BrowserWarning />
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { Routes, Route } from '@openwebf/vue-router';

import BrowserWarning from './components/BrowserWarning.vue';
import HomePage from './Pages/HomePage.vue';
import ButtonPage from './Pages/ButtonPage.vue';
import SwitchPage from './Pages/SwitchPage.vue';
import InputPage from './Pages/InputPage.vue';
import IconPage from './Pages/IconPage.vue';
import SearchInputPage from './Pages/SearchInputPage.vue';
import TextareaPage from './Pages/TextareaPage.vue';
import SegmentedTabPage from './Pages/SegmentedTabPage.vue';
import AlertPage from './Pages/AlertPage.vue';
import DatePickerPage from './Pages/DatePickerPage.vue';
import LoadingPage from './Pages/LoadingPage.vue';
import ModalPopupPage from './Pages/ModalPopupPage.vue';
import PickerPage from './Pages/PickerPage.vue';
import SliderPage from './Pages/SliderPage.vue';
import ContextMenuPage from './Pages/ContextMenuPage.vue';
import CheckboxPage from './Pages/CheckboxPage.vue';
import RadioPage from './Pages/RadioPage.vue';
import TimerPickerPage from './Pages/TimerPickerPage.vue';
import ActionSheetPage from './Pages/ActionSheetPage.vue';
import FormRowPage from './Pages/FormRowPage.vue';
import FormSectionPage from './Pages/FormSectionPage.vue';
import ListTilePage from './Pages/ListTilePage.vue';
import ListSectionPage from './Pages/ListSectionPage.vue';
import TabBarPage from './Pages/TabBarPage.vue';

const isWebF = ref(true);

onMounted(() => {
  // Check if running in WebF by checking for webf global variable
  isWebF.value = typeof window !== 'undefined' && typeof window.webf !== 'undefined';
});
</script>

<style src="./assets/styles/app.css" />