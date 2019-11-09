<script>
	export let name;
	import Draggable from '@shopify/draggable';

let dropzones = document.querySelectorAll('.dropzone');
 
let droppable = new Draggable.Droppable(
  dropzones,
  {
    draggable: '.draggable',
    dropzone:  '.dropzone',
    mirror:    { constrainDimensions: true }
  }
);
console.table(droppable);
</script>

<style>
  body
  {
    display: flex;
  }

  .dropzone
  {
    background: #EEE;
    border:     8px solid black;
    display:    block;
    margin:     16px;
    min-width:  250px;
    padding:    16px;
  }

  .dropzone#alpha { border-color: orangered; }
  .dropzone#beta  { border-color: green;     }
  .dropzone#delta { border-color: skyblue;   }

  .draggable
  {
    background:  #AAA;
    cursor:      move;
    font-weight: bold;
    list-style:  none;
    margin:      4px;
    padding:     8px;
  }
</style>


<div class="dropzone" id="alpha">
  <div class='draggable'>Draggable</div>
</div>

<div class="dropzone" id="beta">

</div>

<div class="dropzone" id="delta">

</div>