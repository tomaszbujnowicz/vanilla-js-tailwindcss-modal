# 🚀 Modal | Vanilla JS TailwindCSS Component

A simple, accessible modal script.

## Requirements
No Node.js, Yarn, NPM, Webpack, Gulp, React, Vue.js etc... just a browser.

## Features
- Vanilla JavaScript
- TailwindCSS
- ARIA attributes
- Data attributes used for JS functionality (semantic and flexible markup)
- Trap focus
- Auto focus on input fields when the modal is opened
- Close a modal with Escape key
- Can be used for multiple modals

## Usage

Trigger via data attributes
```html
<button
  data-modal-trigger
  aria-controls="modal-name"
  aria-expanded="false">
  Open modal
</button>
```

Trigger via a tag
```html
<a
  href="#modal-name-goes-here"
  aria-expanded="false">
  Open from a tag link
</a>
```

### Example markup
```html
<div
  id="modal-name"
  data-modal-target
  class="hidden">
  <div class="flex items-center justify-center fixed inset-0 z-50">
    <div
      data-modal-close
      data-modal-overlay
      tabindex="-1"
      data-class-out="opacity-0"
      data-class-in="opacity-50"
      class="opacity-0 fixed inset-0 w-full z-40 transition-opacity duration-300 bg-black select-none"></div>
    <div
      data-modal-wrapper
      data-class-out="opacity-0 translate-y-5"
      data-class-in="opacity-100 translate-y-0"
      class="opacity-0 translate-y-5 w-full z-50 overflow-auto max-w-md max-h-screen scrolling-touch transition-all duration-300 bg-white flex flex-col transform shadow-xl rounded-md m-5">
      <div class="flex items-center justify-between border-b p-6">
        <div>
          Headline
        </div>
        <button
          data-modal-close
          aria-label="Close"
          class="text-gray-700 hover:text-black focus:outline-none focus:text-black transition ease-in-out duration-150 ml-auto">
          <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" /></svg>
        </button>
      </div>
      <div class="relative overflow-x-hidden overflow-y-auto h-full flex-grow p-5">
        <p class="mb-4">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rem in aliquid nulla, sed veritatis, officiis ea aut natus quas voluptates perferendis ratione modi ab qui omnis cum labore alias eos.
        </p>
        <div class="text-right">
          <button
            data-modal-close
            class="underline">
            Close Modal
          </button>
          or [esc] key
        </div>
      </div>
    </div>
  </div>
</div>
```

## Animations
You can control overlay and the div wrapper animations via data-class-out and data-class-in using TailwindCSS classes

- Leaving screen: `data-class-out` and `class`
- Entering screen: `data-class-in`

```html
<div
  ...
  data-class-out="opacity-0"
  data-class-in="opacity-50"
  class="opacity-0 ..."></div>
  <div
    data-class-out="opacity-0 translate-y-5"
    data-class-in="opacity-100 translate-y-0"
    class="opacity-0 translate-y-5 ...">

```

## Initialize
```javascript
modal.init()
```

## Methods

openModal()
```javascript
modal.openModal('modal-name');
```

closeModal()
```javascript
modal.closeModal('modal-name');
```

### Quick start: Installation
Copy/paste and use.

## Copyright and license
Copyright 2021 Tomasz Bujnowicz under the [MIT license](http://opensource.org/licenses/MIT).
