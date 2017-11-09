# WcfProxy
A POC on generating a proxy for a WCF service and able to call a method  without addding a service reference

Use this Helper class to generate the proxyinstance of the contract defined in wsdl dynamically/programmatically using c#.

The best use of this class is where you dont want to add any servicerefernces to your project and want to just invoke it dynamically/programmatically.

We can invoke the methods dynamically using 

 Sample Usage of the helper class:
 

        private WebServiceProxyHelper helper;

        public Dictionary<string, Object> serviceData = new Dictionary<string, object>();
        
 

Now fill the dictionaries with service details.
            serviceData.Add("WsdlUri", "http://www.webservicex.com/globalweather.asmx?WSDL");
            serviceData.Add("ContractName", "GlobalWeatherSoap");
            serviceData.Add("MethodName", "GetCitiesByCountry");
       
Now call the wsdl proxy by sending parameter "India" to get the cities in the given country 

 var res = helper.GetResponse(serviceData, "India");
 
 
 And the res would be 
 
 <NewDataSet>
  <Table>
    <Country>British Indian Ocean Territory</Country>
    <City>Diego Garcia</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Ahmadabad</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Akola</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Aurangabad Chikalthan Aerodrome</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Bombay / Santacruz</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Bilaspur</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Bhuj-Rudramata</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Belgaum / Sambra</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Bhopal / Bairagarh</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Bhaunagar</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Goa / Dabolim Airport</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Indore</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Jabalpur</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Khandwa</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Kolhapur</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Nagpur Sonegaon</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Rajkot</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Sholapur</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Agartala</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Siliguri</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Bhubaneswar</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Calcutta / Dum Dum</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Car Nicobar</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Gorakhpur</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Gauhati</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Gaya</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Imphal Tulihal</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Jharsuguda</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Jamshedpur</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>North Lakhimpur</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Dibrugarh / Mohanbari</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Port Blair</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Patna</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>M. O. Ranchi</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Agra</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Allahabad / Bamhrauli</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Amritsar</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Varanasi / Babatpur</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Bareilly</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Kanpur / Chakeri</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>New Delhi / Safdarjung</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>New Delhi / Palam</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Gwalior</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Hissar</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Jhansi</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Jodhpur</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Jaipur / Sanganer</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Kota Aerodrome</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Lucknow / Amausi</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Satna</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Udaipur Dabok</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Bellary</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Vijayawada / Gannavaram</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Coimbatore / Peelamedu</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Cochin / Willingdon</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Cuddapah</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Hyderabad Airport</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Madurai</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Mangalore / Bajpe</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Madras / Minambakkam</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Tiruchchirapalli</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Thiruvananthapuram</City>
  </Table>
  <Table>
    <Country>India</Country>
    <City>Vellore</City>
  </Table>
</NewDataSet>
       
       
