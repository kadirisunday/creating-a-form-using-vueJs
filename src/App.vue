<template>
  <div>
    <h3>Payment</h3>
    <form novalidate @submit.prevent="onSave">
      <div class="row">
        <div class="col-md-6">
          <div><strong>Shipping Information</strong></div>
          <div class="form-group">
            <label for="name">Name</label>
            <input type="text" name="" id="name" class="form-control" placeholder="Enter your name" v-model="payment.name">
          </div>
          <div class="form-group">
            <label for="company">Company Name</label>
            <input type="text" name="" id="company" class="form-control" placeholder="Enter your Company Name" v-model="payment.company">
          </div>
          <div class="form-group">
            <label for="address">Address</label>
            <input type="text" name="" id="address" class="form-control" placeholder="Street Address" v-model="payment.address">
          </div>
          <div class="form-group">
            <label for="suite">Suite/Apartment</label>
            <input type="text" name="" id="suite" class="form-control" placeholder="Suite name" v-model="payment.suite">
          </div>
          <div class="form-row">
            <div class="form-group col-md-6">
            <label for="city">City</label>
            <input type="text" name="" id="city" class="form-control" placeholder="City" v-model="payment.city">
          </div>
          <div class="form-group col-md-3">
            <label for="state">state</label>
            <select name="" id="state" class="form-control" v-model="payment.state">
              <option v-for="state in states" 
              :key="state.abbreviation"
              :value="state.abbreviation">
                {{ state.name }}
              </option>
            </select>
          </div>
          <div class="form-group col-md-3">
            <label for="zip">ZIP Code</label>
            <input type="text" name="" id="zip" class="form-control" placeholder="Zip code" v-model="payment.zip">
          </div>
          </div>
          <div class="form-group">
            <input type="submit" value="next" class="btn btn-success" >
          </div>
        </div>
        <div class="col-md-6">
          <div><strong>Billing Information</strong></div>
        </div>
      </div>
    </form>
    <div><pre>{{ payment }}</pre></div>
  </div>
  
</template>

<script>
import { ref } from 'vue';
// import states from '@/lookup/states.js'
export default {
  setup() {
    const payment = ref({
      name:"kadiri sunday",
      company: "corehubng",
    });

    const error = ref("")
    function onSave(){
        alert("Just submit a form");
    }
    return{
      payment,
      onSave
    };
  },
  data(){
    return{
        states: [
  {
      "name": "Alabama",
      "abbreviation": "AL"
  },
  {
      "name": "Alaska",
      "abbreviation": "AK"
  },
  {
      "name": "American Samoa",
      "abbreviation": "AS"
  },
  {
      "name": "Arizona",
      "abbreviation": "AZ"
  },
  {
      "name": "Arkansas",
      "abbreviation": "AR"
  },
  {
      "name": "California",
      "abbreviation": "CA"
  },
  {
      "name": "Colorado",
      "abbreviation": "CO"
  },
  {
      "name": "Connecticut",
      "abbreviation": "CT"
  },
  {
      "name": "Delaware",
      "abbreviation": "DE"
  },
  {
      "name": "District Of Columbia",
      "abbreviation": "DC"
  },
  {
      "name": "Federated States Of Micronesia",
      "abbreviation": "FM"
  },
  {
      "name": "Florida",
      "abbreviation": "FL"
  },
  {
      "name": "Georgia",
      "abbreviation": "GA"
  },
  {
      "name": "Guam",
      "abbreviation": "GU"
  },
  {
      "name": "Hawaii",
      "abbreviation": "HI"
  },
  {
      "name": "Idaho",
      "abbreviation": "ID"
  },
  {
      "name": "Illinois",
      "abbreviation": "IL"
  },
  {
      "name": "Indiana",
      "abbreviation": "IN"
  },
  {
      "name": "Iowa",
      "abbreviation": "IA"
  },
  {
      "name": "Kansas",
      "abbreviation": "KS"
  },
  {
      "name": "Kentucky",
      "abbreviation": "KY"
  },
  {
      "name": "Louisiana",
      "abbreviation": "LA"
  },
  {
      "name": "Maine",
      "abbreviation": "ME"
  },
  {
      "name": "Marshall Islands",
      "abbreviation": "MH"
  },
  {
      "name": "Maryland",
      "abbreviation": "MD"
  },
  {
      "name": "Massachusetts",
      "abbreviation": "MA"
  },
  {
      "name": "Michigan",
      "abbreviation": "MI"
  },
  {
      "name": "Minnesota",
      "abbreviation": "MN"
  },
  {
      "name": "Mississippi",
      "abbreviation": "MS"
  },
  {
      "name": "Missouri",
      "abbreviation": "MO"
  },
  {
      "name": "Montana",
      "abbreviation": "MT"
  },
  {
      "name": "Nebraska",
      "abbreviation": "NE"
  },
  {
      "name": "Nevada",
      "abbreviation": "NV"
  },
  {
      "name": "New Hampshire",
      "abbreviation": "NH"
  },
  {
      "name": "New Jersey",
      "abbreviation": "NJ"
  },
  {
      "name": "New Mexico",
      "abbreviation": "NM"
  },
  {
      "name": "New York",
      "abbreviation": "NY"
  },
  {
      "name": "North Carolina",
      "abbreviation": "NC"
  },
  {
      "name": "North Dakota",
      "abbreviation": "ND"
  },
  {
      "name": "Northern Mariana Islands",
      "abbreviation": "MP"
  },
  {
      "name": "Ohio",
      "abbreviation": "OH"
  },
  {
      "name": "Oklahoma",
      "abbreviation": "OK"
  },
  {
      "name": "Oregon",
      "abbreviation": "OR"
  },
  {
      "name": "Palau",
      "abbreviation": "PW"
  },
  {
      "name": "Pennsylvania",
      "abbreviation": "PA"
  },
  {
      "name": "Puerto Rico",
      "abbreviation": "PR"
  },
  {
      "name": "Rhode Island",
      "abbreviation": "RI"
  },
  {
      "name": "South Carolina",
      "abbreviation": "SC"
  },
  {
      "name": "South Dakota",
      "abbreviation": "SD"
  },
  {
      "name": "Tennessee",
      "abbreviation": "TN"
  },
  {
      "name": "Texas",
      "abbreviation": "TX"
  },
  {
      "name": "Utah",
      "abbreviation": "UT"
  },
  {
      "name": "Vermont",
      "abbreviation": "VT"
  },
  {
      "name": "Virgin Islands",
      "abbreviation": "VI"
  },
  {
      "name": "Virginia",
      "abbreviation": "VA"
  },
  {
      "name": "Washington",
      "abbreviation": "WA"
  },
  {
      "name": "West Virginia",
      "abbreviation": "WV"
  },
  {
      "name": "Wisconsin",
      "abbreviation": "WI"
  },
  {
      "name": "Wyoming",
      "abbreviation": "WY"
  }
]

    }
  
  }
};
</script>