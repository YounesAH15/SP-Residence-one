<script>
	import Tableau from "./tableau.svelte";
    import Where from "./where.svelte";


    const now = Date.now();
    // const today = new Date(now).toISOString();
    const today = new Date(now).toLocaleDateString();
    const madeWhere = "Armentières";
</script>

<form action="/create" method="post">
    <h3>DEMANDEUR</h3>
    
    <div>

        <label for="Nom">
            Nom
            <input type="text" name="" id="">
        </label>

        <label for="Prénom">
            Prénom
            <input type="text" name="" id="">
        </label>

        <label for="Téléphone">
            Téléphone
            <input type="tel" name="" id="">
        </label>

        <label for="Email">
            Email
            <input type="email" name="" id="">
        </label>
    </div>
    
    <div>
        <Where />
    </div>

    <h3>VEHICULE</h3>
    
    <div>

        <label for="Marque">
            Marque
            <input type="text" name="" id="">
        </label>

        <label for="Modèle">
            Modèle
            <input type="text" name="" id="">
        </label>

        <label for="Immatriculation">
            Immatriculation
            <input type="text" name="" id="">
        </label>
    </div>

    <h3>Date et Heure de la prestation</h3>
    
    <div>

        <label for="Le">
            Le
            <input type="date" name="" id="">
        </label>

        <label for="De">
            De
            <input type="time" name="" id="">
        </label>

        <label for="A">
            A
            <input type="time" name="" id="">
        </label>
    </div>

    <h3>LIEU</h3>
    
    <div>
        <Where />
    </div>

    <h3>Forfait par véhicule</h3>
    
    <div>
        <div class="row">
            <Tableau />
            <Tableau />
        </div>
        <div class="row">
            <Tableau />
            <Tableau />
        </div>
    </div>

    <div class="when">
        <label for="faitA">
            A 
            <input value="{madeWhere}">
        </label>
        <label for="Le">
            Le
            <input  value="{today}">
        </label>
    </div>


    <p>
        Le Président <br>
        Mr DUTRIEU David
    </p>
</form>

<style>
    h3 {
        background-color: rgb(255, 204, 127);
        width: 100%;
        margin: 25px 0px;
        font-weight: 500;
        padding-left: 10px;
    }

    div {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;  
        justify-content: space-between;
        align-content: center;
        width: 100%;
    }

    .when {
        display: flex;
        flex-direction: column;
        align-content: flex-start;
    }

    .row {
        display: flex;
        flex-direction: row;

        width: 100%;
    }

    p {
        display: grid;
        justify-content: end;
        padding-bottom: 10vh;
    }

</style>