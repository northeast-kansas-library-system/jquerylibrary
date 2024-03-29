## IntranetUserJS

### SABETHA specific jQuery

#### Title 

* **Developer:** 
* **Date:**
* **Purpose:** 
* **Status:** 
* **Version:** 

```javascript

//SABETHA specific 
  //Adds class to KANOPY allowed attribute 
    $('.SABETHA label:contains("Kanopy (SABETHA):")').parent().addClass('sabethakanopy'); 
  //Adds Kanopy allowed value to new patrons created at SABETHA only on new users 
    var url = $(location).attr('href'); 
    if (url.indexOf("memberentry.pl?op=add") != -1) { 
      $('.sabethakanopy select option[value=SABETHA]').attr("selected", "selected"); 
    } 
  //Changes to Kanopy not allowed when home library is changed to not-SABETHA 
    $('.SABETHA #libraries').change(function() { 
      $('.sabethakanopy select option[value="0"]').attr("selected", "selected"); 
    }); 
  //Changes to Kanopy allowed when home library is changed to SABETHA 
    $('.SABETHA #libraries option[value=SABETHA]').click(function() { 
      $('.sabethakanopy select option[value=SABETHA]').attr("selected", "selected"); 
    }); 

```

#### Notes:

This adds a Kanopy permission setting to users with a SABETHA home library when SABETHA staff add or edit new borrowers.  

