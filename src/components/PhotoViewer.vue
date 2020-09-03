<!-- eslint-disable -->

<template>
  <div class="space-y-4 flex-col flex-wrap">
    <div class="border shadow-sm border-gray-200 rounded-lg p-0.5 w-full">
      <img :src="images[imageIndex].src" alt="" />
    </div>
    <div class="">
      <ListBox
        role="tablist"
        ref="tablist"
        class="flex flex-row space-x-4 lg:space-x-2 justify-between"
      >
        <ListOptions
          v-for="(image, index) in images"
          :key="image.id"
          :title="image.title"
          @onArrowRightPressed="toggleRight(index)"
          @onClick="handleImageToggle(index)"
          @onArrowLeftPressed="toggleLeft(index)"
          class="hover:border hover:border-gray-400 focus:border focus:border-gray-400 focus:shadow-sm focus:outline-none"
          :class="{ 'border-2 border-gray-700': index === imageIndex }"
        >
          <img :src="image.src" :alt="image.title" />
        </ListOptions>
      </ListBox>
    </div>
  </div>
</template>



<script>

import ListBox from './ListBox';
import ListOptions from './ListBoxOptions';

const image = require.context('../../public/img', true , /\.jpg$/); 


const images = [
    { 
        id:1,
        title: 'kemper front photo',
        src: image('./kemper-front.jpg')
    },
    {
        id:2,
        title: 'kemper angle photo',
        src: image('./kemper-angle.jpg') 
    },
    {
        id:3,
        title: 'kemper rear photo',
        src: image('./kemper-rear.jpg')
    }
];
 

export default {
    

    name: 'PhotoViewer',
    components: {
        ListBox,
        ListOptions
    },
    data: () => ({
        images,
        imageIndex: 0,
        isSelected: false,
        tabs: [],
        tablist: null,
        keys: {
          left: 37,
          right: 39,
        },
        direction: {
            37: -1,
            39: 1
        },
         
    }), 
    mounted() {
      this.tablist = this.$refs.tablist;
    },
    created() {
        
        this.generateArrays();

        for(let i = 0; i< this.tabs.length; ++i) {
          this.addListeners(i);
        }

        
    },
    methods: {
      handleImageToggle(index) {
          return this.imageIndex = index;
      },

      toggleRight() {
       return this.imageIndex <= 1 ? this.imageIndex ++ : this.imageIndex = 0
      },
      toggleLeft() {
        return this.imageIndex >= 1 ? this.imageIndex -- : this.imageIndex = 2
      },
      generateArrays() {
        this.tabs = document.querySelectorAll('[role="tab"]');
      },

       addListeners (index) {
    this.tabs[index].addEventListener('click', this.clickEventListener);
    // this.tabs[index].addEventListener('keydown', this.keydownEventListener);
    this.tabs[index].addEventListener('keyup', this.keyupEventListener);

    // Build an array with all tabs (<button>s) in it
    this.tabs[index].index = index;
  },

      clickEventListener (event) {
    var tab = event.target;
    this.activateTab(tab, false);
  },


    keydownEventListener (event) {
    var key = event.keyCode;

    switch (key) {
      case this.keys.end:
        event.preventDefault();
        // Activate last tab
        this.activateTab(this.tabs[this.tabs.length - 1]);
        break;
      case this.keys.home:
        event.preventDefault();
        // Activate first tab
        this.activateTab(this.tabs[0]);
        break;

      // Up and down are in keydown
      // because we need to prevent page scroll >:)
      case this.keys.up:
      case this.keys.down:
      this.switchTabOnArrowPress(event);
        break;
    }
  },

  keyupEventListener (event) {
    var key = event.keyCode;

    switch (key) {
      case this.keys.left:
      case this.keys.right:
      this.switchTabOnArrowPress(event);
        break;
      
    }
  },


   switchTabOnArrowPress (event) {
    var pressed = event.keyCode;

    for (let x = 0; x < this.tabs.length; x++) {
      this.tabs[x].addEventListener('focus', this.focusEventHandler);
    }

    if (this.direction[pressed]) {
      var target = event.target;
      if (target.index !== undefined) {
        if (this.tabs[target.index + this.direction[pressed]]) {
          this.tabs[target.index + this.direction[pressed]].focus();
        }
        else if (pressed === this.keys.left || pressed === this.keys.up) {
          this.focusLastTab();
        }
        else if (pressed === this.keys.right || pressed == this.keys.down) {
          this.focusFirstTab();
        }
      }
    }
  },


     activateTab (tab, setFocus) {
    setFocus = setFocus || true;
    // Deactivate all other tabs
      this.deactivateTabs();

    // Remove tabindex attribute
    tab.removeAttribute('tabindex');

    // Set the tab as selected
    tab.setAttribute('aria-selected', 'true');

    // Set focus when required
    if (setFocus) {
      tab.focus();
    }
  },

   deactivateTabs () {
    for (let t = 0; t < this.tabs.length; t++) {
      this.tabs[t].setAttribute('tabindex', '-1');
      this.tabs[t].setAttribute('aria-selected', 'false');
      this.tabs[t].removeEventListener('focus', this.focusEventHandler);
    }},

   focusFirstTab () {
    this.tabs[0].focus();
  },

  
   focusLastTab () {
    this.tabs[this.tabs.length - 1].focus();
  },

   focusEventHandler (event) {
    var target = event.target;

    setTimeout(this.checkTabFocus, 1, target);
  },

   checkTabFocus (target) {
    let focused = document.activeElement;

    if (target === focused) {
      this.activateTab(target, false);
    }
  },
  }
}


</script>