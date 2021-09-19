
#Javascript - Day -8 : MRF - array method


// Get all the countries from Asia continent /region using Filter function
fetch("https://restcountries.eu/rest/v2/all").then(res=>res.json())
.then(res=>{

    console.log(res.filter(val=>val.region=="Asia"));

});

// Get all the countries with a population of less than 2 lakhs using Filter function
fetch("https://restcountries.eu/rest/v2/all").then(res=>res.json())
.then(res=>{

    console.log(res.filter(val=>val.population<200000));

});

// Print the following details name, capital, flag using forEach function
fetch("https://restcountries.eu/rest/v2/all").then(res=>res.json())
.then(res=>{

    res.forEach(element => {
            console.log(element.name,element.capital,element.flag);
    });


});

// Print the total population of countries using reduce function
fetch("https://restcountries.eu/rest/v2/all").then(res=>res.json())
.then(res=>{
       console.log(res.reduce((accu,next)=> accu + next.population, 0));

});

// Print the country which uses US Dollars as currency.

fetch("https://restcountries.eu/rest/v2/all").then(res=>res.json())
.then(res=>{

    console.log(res.filter(val=>val.currencies[0].code=="USD"));


})
