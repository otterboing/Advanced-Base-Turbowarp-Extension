## Check it out:
[DefaultExtension.js](/DefaultExtension.js)

## Use how you like.

Though it may have the MIT license all around it, this base extension has no actual license.

Those are simply there for my own convenience and how I think most extensions should be licensed. 

So use and publish it however you want!

## Credit is not required.
Though it is appreicated!

---

# Usage

This base extension adds some functions that I find to be highly useful:

- BT : == `Scratch.BlockType`
- AT : == `Scratch.ArgumentType`
- BR : == `'---',` | Break

- makeBlock : Removes the most time consuming process in setup.
  ```javascript
  makeBlock('opcode', BT.BLOCK_TYPE, 'Block text.', {'arguments':ARG()}, {extra: 'Extra stuff here', blockIconURI: 'url'});
  
  // Example:
  makeBlock('turnPlayer', BT.COMMAND, 'Turn player [degrees] degrees', {
    degrees: ARG(AT.ANGLE, 0)
  }, {blockIconURI: 'compass.png'});


  // Would usually be:
  {
    opcode: 'turnPlayer',
    blockType: Scratch.BlockType.COMMAND,
    text: 'Turn player [degrees] degrees',
    blockIconURI: 'compass.png',
    arguments: {
      degrees: {
        type: Scratch.ArgumentType.ANGLE,
        defaultValue: 0
      }
    }
  }
  ```
- ARG : Argument shortened
  ```javascript
    ARG(AT.ARGUMENT_TYPE, 'defaultValue', 'menu_name (optional)');
  
    //Example:
    {
      target: ARG(AT.STRING, 'This Sprite', 'sprites');
    }
  
  
  // Would usually be:
  {
    target: {
      type: Scratch.ArgumentType.STRING,
      defaultValue: 'This Sprite',
      menu: 'sprites'
    }
  }
  ```
- makeButton : Makes easy buttons
  ```javascript
    makeButton('Button Text', 'buttonFunction');


    // Would usually be:
    {
      blockType: Scratch.BlockType.BUTTON,
      text: 'Button Text',
      func: 'buttonFunction'
    }
  ```
- label : Makes a label
  ```javascript
    label('Label Text');


    // Would usually be
    {
      blockType: 'label',
      text: 'Label Text'
    }

---

### See the rest of my extensions:
https://github.com/otterboing/Otterboings-Turbowarp-Extensions

<sub>(These are licensed... Under MIT 😎)</sub>

#### Or my website:

https://otterboing.neocities.org
