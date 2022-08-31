import { StatusBar } from 'expo-status-bar';
import React, { Component } from 'react';
import { StyleSheet, Text, View,TouchableOpacity,FlatList} from 'react-native';
import axios from 'axios';
import { render } from 'react-dom';

class App extends React.Component{
  constructor()
{
  super()
  this.state={
    data:[]
  }
}


componentDidMount()
{
  this.getapiData()
}
async getapiData()
{
  console.log('Hello')
  let resp=await axios.get('https://reactnative.dev/movies.json')
  console.warn(resp.data.movies)
  console.log(resp.data.movies)
  this.setState({data:resp.data.movies})
}
render(){
return(

  
       <View style={{flex:1,margin:70}}> 
        {
          this.state.data.length>0?
          <View>
            {
              this.state.data.map((item)=>
              <Text style={{fontSize:20}}>{item.title},{item.releaseYear}</Text>
              )
            }
            </View>:<Text>data is loading</Text>
        }

<View>

<TouchableOpacity
    style={styles.OTP}
    onPress={()=> this.getapiData()}
    >
      <Text style={styles.Bt}>Fetch Data</Text>
      </TouchableOpacity>   
      </View>
  </View> 
  
)
}
}
const styles=StyleSheet.create({
  textBox:{
    borderColor:'green',
    borderwidth:2,
    padding:10,
    marginTop:30,
    marginHorizontal:20,
    marginVertical:30,
    backgroundColor:'grey',
    borderRightColor:'gold',
    text:'black'
  },
})



export default App;
