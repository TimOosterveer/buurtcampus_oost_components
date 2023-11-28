

<form>
    <label for="name">Voornaam:</label>
    <input type="text" id="name" name="name" placeholder="Voer je voornaam in">

    <label for="lastname">Achternaam:</label>
    <input type="text" id="lastname" name="lastname" placeholder="Voer je achternaam in">

    <label for="message">Bericht:</label>
    <textarea id="message" name="message" cols="30" rows="10" placeholder="Typ hier je bericht"></textarea>

    <input type="submit" value="Verzenden">
</form>

<style>
  
    form{
        display: flex;
        flex-direction: column;
        width: 25rem;
        background-color: var(--background-color-light);
        padding: var(--padding);
        border-radius: var(--bradius);
    }
</style>