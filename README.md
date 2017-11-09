# WcfProxy
A POC on generating a proxy for a WCF service and able to call a method  without addding a service reference

Use this Helper class to generate the proxyinstance of the contract defined in wsdl dynamically/programmatically using c#

We can invoke the methods dynamically using 

  public abstract object Invoke(object obj, BindingFlags invokeAttr, Binder binder, object[] parameters, CultureInfo culture);
  
 
