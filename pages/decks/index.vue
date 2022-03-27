<template>
  <div>
    <h1>Your Decks, please enter number of deck to show:</h1>
    <input
      v-model="deckID"
      type="text"
      placeholder="Please enter decksID"
    >
    <button @click="showDeck">
      Go to Deck
    </button>
  </div>
</template>

<script>
export default {
  /* kết nối API với serve thường như thế sẽ mất một khoảng thời gian nhất định tầm 1,5s
   sẽ có dự liệu
  */
  data () {
    return {
      deckID: 1
    }
  },
  created () {
    setTimeout(() => {
      this.decks = [
        {
          _id: 1,
          name: 'Learn English',
          description: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Culpa quas, sequi adipisci eaque, vero ab ratione rerum expedita, aut praesentium sint reprehenderit. Similique et quis totam tenetur autem deserunt ea.',
          thumbnail: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4f_EFOqkRyKqXrhvtXrs-Rj48KB6fShDJow&usqp=CAU'
        },
        {
          _id: 2,
          name: 'Learn Chinese',
          description: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Culpa quas, sequi adipisci eaque, vero ab ratione rerum expedita, aut praesentium sint reprehenderit. Similique et quis totam tenetur autem deserunt ea.',
          thumbnail: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4f_EFOqkRyKqXrhvtXrs-Rj48KB6fShDJow&usqp=CAU'
        },
        {
          _id: 3,
          name: 'Learn Japanese',
          description: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Culpa quas, sequi adipisci eaque, vero ab ratione rerum expedita, aut praesentium sint reprehenderit. Similique et quis totam tenetur autem deserunt ea.',
          thumbnail: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4f_EFOqkRyKqXrhvtXrs-Rj48KB6fShDJow&usqp=CAU'
        }
      ]
    }, 1500)
  },
  methods: {
    showDeck () {
      this.$router.push(`/decks/${this.deckID}`)
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
