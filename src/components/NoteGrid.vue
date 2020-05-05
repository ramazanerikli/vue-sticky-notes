<template>
        <div class="noteContainer">
            <div @click="note.editing = !note.editing" v-for="(note, index) in filteredNotes" :key="`note-${index}`" class="note" :style="{'background-color': note.theme}">
                <div>
                    <span v-if="note.editing" @click.prevent="deleteNote(index)" class="delete"><i class="fas fa-times"></i></span> 
                    <span contenteditable="true" >{{ note.title}}</span>
                    <p contenteditable="true" class="note-text">{{ note.text }}</p>
                </div>
            </div>
        </div>
</template>

<script>
    export default {
        props: ['notes'],
        data: function() {
            return {
                selectedTheme: '',
                theme: 'all'
            }
        },
	computed: {
		filteredNotes: function() {
			var vm = this;
			var theme = vm.selectedTheme;
			
			if(theme === "all") {
				return vm.notes;
			} else {
				return vm.notes.filter(function(note) {
					return note.theme === theme;
				});
			}
		}
	},
    }
</script>