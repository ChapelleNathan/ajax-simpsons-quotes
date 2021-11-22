function fetchSimpsonQuotesJSON()
{
    const url = 'https://simpsons-quotes-api.herokuapp.com/quotes';
    axios.get(url)
        .then(function(response) {
            return response.data;
        })
        .then(function(simpson) {
            console.log('Data decoded from JSON:', simpson);
            const simpsonQuoteHtml = `
                <h2>${simpson[0]['character']}</h2>
                <img src = "${simpson[0]['image']}" alt = "image of ${simpson[0]['character']}">
                <p>${simpson[0]['quote']}</p>
                `;
                document.querySelector('#simpsonQuote').innerHTML = simpsonQuoteHtml;
        })
}

fetchSimpsonQuotesJSON();