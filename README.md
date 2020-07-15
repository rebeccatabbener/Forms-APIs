# Forms-APIs
The JS:
const myForm = document.querySelector('#the-form');
myForm.addEventListener("submit", makeCard);


const h1 = document.querySelector('#cardGreeting')
const p = document.querySelector('#type-of-event')
const message = document.querySelector('#cardMessage')
function makeCard(e){
        e.preventDefault();
        const userGreeting = e.target.greeting.value;
        const userEvent = e.target.events.value;
        const userMessage = e.target.message.value;
        console.log(userGreeting, userEvent, userMessage);
        h1.textContent = userGreeting;
        p.textContent= `Have a wonderful ${userEvent}`;
        message.textContent= userMessage;

        
        
}

The HTML:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Celebration Card</title>
    <script defer src="/Users/rebeccatabbener/Documents/Development/greetingCard/action.js"></script>
</head>
<body>
    <form id="the-form" >
        <label for="greeting">Greeting:</label>
        <input id="greeting" type="text" placeholder="Greeting">
        <label for="events">Type of event:</label>
        <select id="events" name="cars">
            <option value="newyear">New Year</option>
            <option value="christmas">Christmas</option>
            <option value="easter">Easter</option>
          </select>
        <label for="message">Message:</label>
        <input id="message" type="text" placeholder="Message">
        <input id= "submit" type="submit" value="send">
    </form>
    <section>
        <h1 id="cardGreeting"></h1>
        <p id="type-of-event"> </p>
        <p id="cardMessage"></p>
    </section>
</body>
</html>
