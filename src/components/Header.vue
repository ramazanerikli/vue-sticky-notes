<template>
    <div class="header">
      <ul class="categories">
        <li>
          <a>
            <input @click="$emit('change-category', 'all')" v-model="category" type="radio" value="all" id="10">
            <label for="10" style="background: #fff"></label>
            All
          </a>
        </li>

        <li>
          <a>
            <input @click="$emit('change-category', '#FF8A80')" v-model="category"  type="radio" value="#FF8A80" id="11">
            <label for="11" style="background: #FF8A80"></label>
            Key
          </a>
        </li>

        <li>
          <a>
            <input @click="$emit('change-category', '#FFFF8D')" v-model="category" type="radio" value="#FFFF8D" id="12">
            <label for="12" style="background: #FFFF8D"></label>
            To Read
          </a>
        </li>

        <li>
          <a>
            <input @click="$emit('change-category', '#CCFF90')" v-model="category" type="radio" value="#CCFF90" id="13">
            <label for="13" style="background: #CCFF90"></label>
            To Watch
          </a>
        </li>

        <li>
          <a>
            <input @click="$emit('change-category', '#80D8FF')" v-model="category" type="radio" value="#80D8FF" id="14">
            <label for="14" style="background: #80D8FF"></label>
            To Do
          </a>
        </li>

        <li>
          <a>
            <input @click="$emit('change-category', '#DDA0DD')" v-model="category" type="radio" value="#DDA0DD" id="15">
            <label for="15" style="background: #DDA0DD"></label>
            Event
          </a>
        </li>

    </ul>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                category: ''
            }
        },
    }
</script>