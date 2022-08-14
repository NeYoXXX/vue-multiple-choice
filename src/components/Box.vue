<script setup>
import BoxConent from './BoxConent.vue'
import tippy from 'tippy.js';
import { createApp, getCurrentInstance, nextTick, onMounted } from 'vue';

// console.log(BoxConent.render());




const props = defineProps({
  target: {
    type:String,
    required: true
  },
  options:{
    type:Array,
    default:()=>[]
  }
})
 
// const boxConent = createApp(BoxConent,{
//     props:props.options
// })

// console.log(boxConent,'boxConent');
const ins = getCurrentInstance()
console.log(ins,'ins');

nextTick(()=>{

    const div = document.createElement('div')

    tippy(`#${props.target}`, {
        content: '<strong>Bolded content</strong>',
        allowHTML: true,
    });
})



console.log(props.target);





</script>