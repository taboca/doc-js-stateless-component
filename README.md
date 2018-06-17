# Stateless components and application states 

## Question - One emerging question here was that right upfront I have stumbled in something called stateless

The following was the kind of component that I was coding, which came out of [1] a React simple todo list example: 

```

import React, { Component } from 'react'
import { connect } from 'react-redux'
import { addList } from '../actions'


import {
    Button,
    View,
    TextInput,
} from 'react-native';

const AddList = () => {
  let input

  this.handleClick = function () {
	// how to access the TextInput? 
  }

  return (
    <View>

      <TextInput
              style={{height: 40}}
              placeholder="This is a text" ref="myInput"
            />

      <Button
       onPress={this.handleClick}
       title="Click handler"
       color="gray"
       accessibilityLabel="Click this button to access the handler"
      />
  </View>
  )
}

export default connect()(AddList)

```

## Where the arguments come from? - and the concept destructuring in the context of React  

Let's look at the following example: 

```

import React from ‘react’;

const HelloWorld = ({name}) => (
 <div>{`Hi ${name}`}</div>
);

export default HelloWorld;

```

Which was taken from [2016 Cory]. This is an example of a functional component; that, because this is mostly a function that is being used in the context of React as a component to render data based on certain inputs - with no logic. 

[2016 Cory](https://hackernoon.com/react-stateless-functional-components-nine-wins-you-might-have-overlooked-997b0d933dbc)

Now, a question is "where does name come from?" 

First, we need to look at destructuring, of Destructuring assignment [1]. 

[1](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) 


## Stateless components - WTF are the arguments? 

* Suddently there is a function in there, such as "dispatch", for accessing the necessary infrastructure of communication with the store; 

* Suddently some of the samples show some properties; 

* Is this related to React vs React Redux; 

* Is this related to ES6
