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


## Stateless components - WTF are the arguments? 

* Suddently there is a function in there, such as "dispatch", for accessing the necessary infrastructure of communication with the store; 

* Suddently some of the samples show some properties; 

* Is this related to React vs React Redux; 

* Is this related to ES6
