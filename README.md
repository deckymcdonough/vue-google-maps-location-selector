vue-google-maps-location-selector
=============

A vuejs google maps component that allows latitude and longitude to be selected from a map interface.

## Installation
---------------
##npm
``` sh
npm install --save vue-stripe-card-form
```

Include the stripe script in the head of your index.html file
``` html
<script type="text/javascript" src="https://js.stripe.com/v2/"></script>
```

Use the component by passing though your stripe publishable key.
The `tokenReceived` event will fire as soon as the form recieves a token from the Stripe API.
``` html
<stripe-payment @tokenReceived="gotToken" :stripe-key="[YOUR_STRIPE_PUBLISHABLE_KEY_GOES_HERE]">
</stripe-payment>
```

You can get the token in the callback function defined in the `tokenReceived` event.
``` javascript
methods:{
    gotToken(token){
        // Send your token to the server or whatever
    }
}
```
