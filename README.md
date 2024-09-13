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
