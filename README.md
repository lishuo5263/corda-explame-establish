# corda-explame-establish


When I was build offcial corda-example project ,I have some wrong with project ,the console info is: miss anjs jar, but I saw the project contain this jar ? WTF??  finally I upgrade By System jdk environment to 1.8.151 to finish this problem .


Run Coradapp
1:following offcial document https://docs.corda.net/hello-world-state.html
 In java we do like this :
 1)rename the TemplateState.java to IOUState.java.
 2)add some entity code to IOUState.java. make this class like JavaBean
 
 In kotlin we do like this :
 1)opening TemplateState.java (for Java) or App.kt (for Kotlin)
 2)add some coke like this
  import net.corda.core.contracts.ContractState
  import net.corda.core.identity.Party

  class IOUState(val value: Int,
                 val lender: Party,
                 val borrower: Party) : ContractState {
      override val participants get() = listOf(lender, borrower)
  }

2: add owe IOUFlow

3: step by 2 then add owe IOUFlowResponder

4: step by 3 then add owe IOUContract
