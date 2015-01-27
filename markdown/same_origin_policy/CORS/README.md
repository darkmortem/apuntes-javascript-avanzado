# CORS

<sub>[http://enable-cors.org/](http://enable-cors.org/)</sub>  
<sub>[http://www.nczonline.net/blog/2010/05/25/cross-domain-ajax-with-cross-origin-resource-sharing/](http://www.nczonline.net/blog/2010/05/25/cross-domain-ajax-with-cross-origin-resource-sharing/)</sub>  
<sub>[http://www.w3.org/TR/cors/](http://www.w3.org/TR/cors/)</sub>

**Cross-Origin Resource Sharing** (CORS) permite realizar peticiones a otros dominios siempre y cuando el dominio de destino (servidor) esté de acuerdo en recibir peticiones del dominio de origen. 

Es una tecnología ([especificación W3C](http://www.w3.org/TR/cors/)) [implementada en los navegadores actuales](http://caniuse.com/#feat=cors), que intercambia ciertas cabeceras HTTP con el servidor de destino para saber si debe permitir o no el intercambio de datos.

Cada vez más [API's publicas](http://enable-cors.org/resources.html#apis) [permiten CORS](http://www.w3.org/wiki/CORS_Enabled#Who_is_doing_it_already.3F) pero la mayoria ofrecen solo [JSONP](http://www.programmableweb.com/category/all/apis?data_format=21174).

## Peticiones CORS sencillas

- con **jQuery**

    <sub>[Ejemplo CORS request (HTML)](http://jsfiddle.net/juanma/rL7o58rr/)</sub>  
    <sub>[Ejemplo CORS request (JSON)](http://jsfiddle.net/juanma/w1bbehqz/)</sub>

    Una peticion CORS utilizando jQuery es, en la mayoria de los casos, transparente al cliente, ya que si [nuestro navegador lo soporta](https://test-cors.appspot.com/#technical) y el servidor (por ejemplo [GitHub](https://developer.github.com/v3/#cross-origin-resource-sharing)) está preparado, puede ser tan sencillo como esto:

    ```javascript
    $.ajax({
        url: "https://api.github.com/users/juanmaguitar/repos",
        success: function( response_json ) {
            console.info (response_json);
        }
    });
    ```



    https://remysharp.com/2011/04/21/getting-cors-working
    http://pixelsvsbytes.com/blog/2011/12/ajax-cross-domain-requests-with-cors/

    http://www.html5rocks.com/en/tutorials/file/xhr2/#toc-cors

    https://remysharp.com/2011/04/21/getting-cors-working
    https://remysharp.com/2013/01/14/cors-isnt-just-for-xhr

    http://www.eriwen.com/javascript/how-to-cors/   
    https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS  

    http://client.cors-api.appspot.com/client  
    http://www.html5rocks.com/en/tutorials/cors/?redirect_from_locale=es  
    http://www.eriwen.com/javascript/how-to-cors/  
    http://enable-cors.org/  
    https://developers.google.com/api-client-library/javascript/features/cors  