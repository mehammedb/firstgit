# firstgit
*****what i grasp in usestate*****  
  
setState in class component and setter methon in useState hook are the same.
both executes in bach.  
if there are many setter method and if they receive the argument other than function, Only the last method will be executed.  
But if they receive function as argument, they execute all  
setter method in class component can merge but in useState you should do it manually  
newLine1


any jsx tag needs key property if it is iterated. key pro can not be accessed in child component

pure class component vs regular class component  
pure re-renders if prevstate and/or prevProp differs from current in shallow comparision.(===)  
regular component always re-renders since the componentShouldUpdate value is always true  
we can export functional components using react.memo() to substitute pure class components with functional components(pure class component = memo functional component)  


portal is render component outside of root id, it uses for modal..  
HOC/high order components are functions that receive component as argument and return it with props(counter state and increement method)  
dont forget {...this.props} if there are other props in the up of HOC functions.  


#useeffect  
is to perform sideeffects like updating the DOM & data fetching from API.  
is replacement of componentdidmount,willunmount & didupdate.  
will be executed after every rendder of component if no dependency. empty array means once. so focus on its dependency for performancr issue.  
returned function inside callback of use effect method is executed when unmounting. so use cleanup method there.  
deffinig function inside useefect is better


  # DATE  
    
date from node to datetime: as it is  
date from node to timestamp: as it is but assuming the timezone as system's timezone regardless of session time zone  

date from itself db to db: bothe takes date as it is like above example. but timestamp here takes timezone from session not system. if we take date now() from itself from db, it will lead us to error if field type is datetime and session is out of our assumption  
but timezone is explicitly define, nodejs first convert it into systems timezon and send to mysql while mysql session timezon also converts it into its own session timezon and insert it.

