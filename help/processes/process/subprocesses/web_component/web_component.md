## Web Component
Display a component within the chat.

For example the following Web component defines a Web component with the tag `hello-world`. To integrate the Web component in LoyJoy, (1) deploy the following JavaScript snippet as a file to a Web hosting of your choice, (2) enter the URL to this file in LoyJoy as the URL of Web component and (3) enter `hello-world` as the HTML tag of the Web component.

```
(function () {
  class HelloWorld extends HTMLElement {
    constructor () {
      super()
      this.attachShadow({ mode: 'open' })

      /*
      * sic! firefox requires methods to be defined in constructor
      */

      this.someAttribute = () => this.attributes['foo']?.value

      this.render = () => {
        this.shadowRoot.innerHTML = `
          <div class="hello-world">
            Hello world
          </div>
        `

        const helloWorld = this.shadowRoot.querySelector('.hello-world');

        helloWorld.onclick = () => {
          this.dispatchEvent(new CustomEvent('hello', { detail: { foo: this.someAttribute } }))
        }
      }
    }

    connectedCallback() {
      if (!this._rendered) {
        this.render()
        this._rendered = true
      }
    }
  }

  if (!customElements.get('hello-world')) {
    customElements.define('hello-world', HelloWorld)
  }
})()
```
