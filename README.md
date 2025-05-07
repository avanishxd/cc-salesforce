public class CalciController {
    public Integer a {get; set;}
    public Integer b {get; set;}
    public Integer result {get; set;}
    public String operation {get; set;}
    
    public void add(){
        result=a+b;
    }
    public void sub(){
        result=a-b;
    }
    public void mul(){
        result=a*b;
    }
    public void div(){
        result=a/b;
    }
}


<apex:page controller="CalciController">
    <h1 style="margin:10px; font-size:20px">Basic Calculator</h1><br/><br/>

    <apex:form >
        <label for="first" style="margin:10px">Enter First Number </label>
        <apex:inputText value="{!a}" id="first"/><br/><br/>
        <label for="second" style="margin:10px">Enter Second Number </label>
        <apex:inputText value="{!b}" id="second"/><br/><br/>
        
        <apex:commandButton value="Add" action="{!add}" style="margin:10px"/>
        <apex:commandButton value="Subtract" action="{!sub}" style="margin:10px"/>
        <apex:commandButton value="Multiply" action="{!mul}" style="margin:10px"/>
        <apex:commandButton value="Divide" action="{!div}" style="margin:10px"/>

        <br/>

        <p style="margin:10px"><strong>Result: {!result}</strong></p>
    </apex:form>
</apex:page>
