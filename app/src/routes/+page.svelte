
<script>
	import { onMount } from 'svelte';
  import Form from '../components/forms/form.svelte';

  function exportHTMLtoPDF() {
     let htmlElement = document.getElementById('content');
      console.log(htmlElement)
      let opt = {
  filename:     'myfile.pdf',
  image:        { type: 'jpeg', quality: 0.98 },
  html2canvas:  { scale: 4,},
  jsPDF:        { unit: 'em', format: 'legal', orientation: 'portrait' }
};
     html2pdf().from(htmlElement).set(opt).save();
  }

  onMount(()=>{
    let exportButton = document.getElementById('exportButton')
    if(!exportButton) {
      console.log("no export button in document found")
      return;
    }
    exportButton.addEventListener('click', exportHTMLtoPDF);
  })
</script>

<div id="content">
  <div id="title">
    <img src="" alt="">
    CONTRAT DE PRESTATION POUR VEHICULES
  </div>
  <Form />
</div>
<!-- <button id="exportButton">
  Export
</button> -->
<style>
  #title {
    display: flex;
    flex-direction: row;
    font-size: x-large;
    justify-content: space-around;
    align-items: center;

    margin-top: 5vh;
  }

  img {
    min-height: 15vh;
    min-width: 15vw;
  }

</style>