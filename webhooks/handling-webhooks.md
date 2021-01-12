# Handling Webhooks

The first step to adding WebHooks to your account is to build your own custom endpoint. Creating a WebHook endpoint on your server is no different from creating any page on your website. With PHP, you might create a new .php file on your server; with a Ruby framework like Sinatra, you would add a new route with the desired URL.

## Key Considerations

For each event occurrence, Trust Swiftly POSTs the WebHook data to your endpoint in JSON format. The full event details are included and can be used directly after parsing the JSON into an Event object. Thus, at minimum, the WebHook endpoint needs to expect data through a POST request and confirm successful receipt of that data. Beyond those two concepts, you should also…

**Return a 2xx status code quickly**

To acknowledge receipt of an event, your endpoint must return a 2xx HTTP status code to Trust Swiftly. All response codes outside this range, including 3xx codes, indicate to Trust Swiftly that you did not receive the event.

**Signature Verification**

Your app must verify that notification messages originated from Trust Swiftly, w**h**ere not altered or corrupted during transmission, where targeted for you, and contain a valid signature. For each WebHook that is sent we also include a HTTP header for you to validate against to ensure the data we send is the data you're receiving!
