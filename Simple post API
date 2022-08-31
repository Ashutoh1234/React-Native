import React from "react";
import { StyleSheet,Text,View } from "react-native";

export default class App extends React.Component{

async componentDidMount(){
    try{
        await fetch('https://webhook.site/155abb53-f9de-42f2-913c-4497bbbc7bf3',{
            method: 'post',
            mode: 'no-cors',
            headers:{
                'Accept':'application/json',
                'Content-Type':'application/json'
            },
            body:JSON.stringify({
                username:'Ashu',
                password:'1234'
            })
        }
        );
    }catch(e){
        console.log(e);
    }
}
render(){
    return(
        <View><Text>Hello</Text></View>
    );
}


}
