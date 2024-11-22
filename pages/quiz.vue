<template>
  <div class="quiz-container">
    <h1>Evaluación de Conocimientos</h1>
    
    <div class="quiz-box" v-for="(question, index) in questions" :key="index">
      <h3>Pregunta {{ index + 1 }}</h3>
      <p>{{ question.text }}</p>
      
      <div class="options">
        <label v-for="(option, optIndex) in question.options" :key="optIndex" class="option">
          <input 
            type="radio" 
            :name="'question-' + index"
            :value="option"
            v-model="question.selectedAnswer"
          >
          {{ option }}
        </label>
      </div>
      
      <button @click="checkAnswer(index)" class="check-btn">Verificar Respuesta</button>
      
      <div v-if="question.showResult" 
           :class="['result', question.isCorrect ? 'correct' : 'incorrect']">
        {{ question.isCorrect ? '¡Correcto!' : 'Incorrecto. Intenta de nuevo.' }}
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const questions = ref([
  {
    text: "¿Qué es el movimiento rectilíneo uniforme?",
    options: [
      "Movimiento con velocidad constante en línea recta",
      "Movimiento en círculos",
      "Movimiento con aceleración variable",
      "Movimiento en zigzag"
    ],
    correctAnswer: "Movimiento con velocidad constante en línea recta",
    selectedAnswer: "",
    showResult: false,
    isCorrect: false
  },
  {
    text: "¿Cuál es la unidad de medida de la velocidad en el SI?",
    options: [
      "Metros por segundo (m/s)",
      "Kilómetros por hora (km/h)",
      "Millas por hora (mph)",
      "Centímetros por segundo (cm/s)"
    ],
    correctAnswer: "Metros por segundo (m/s)",
    selectedAnswer: "",
    showResult: false,
    isCorrect: false
  },
  {
    text: "¿Qué es la aceleración?",
    options: [
      "Cambio de velocidad en el tiempo",
      "Distancia recorrida",
      "Velocidad constante",
      "Posición final"
    ],
    correctAnswer: "Cambio de velocidad en el tiempo",
    selectedAnswer: "",
    showResult: false,
    isCorrect: false
  }
])

const checkAnswer = (index) => {
  const question = questions.value[index]
  question.showResult = true
  question.isCorrect = question.selectedAnswer === question.correctAnswer
}
</script>

<style scoped>
.quiz-container {
  padding: 20px;
  max-width: 800px;
  margin: 0 auto;
}

h1 {
  color: #2c3e50;
  text-align: center;
  margin-bottom: 40px;
}

.quiz-box {
  background-color: #f8f9fa;
  padding: 25px;
  border-radius: 10px;
  margin-bottom: 30px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

h3 {
  color: #3498db;
  margin-bottom: 15px;
}

.options {
  display: flex;
  flex-direction: column;
  gap: 15px;
  margin: 20px 0;
}

.option {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 10px;
  background-color: white;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.option:hover {
  background-color: #e8f4f8;
}

.check-btn {
  background-color: #3498db;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.check-btn:hover {
  background-color: #2980b9;
}

.result {
  margin-top: 15px;
  padding: 10px;
  border-radius: 5px;
  text-align: center;
}

.correct {
  background-color: #2ecc71;
  color: white;
}

.incorrect {
  background-color: #e74c3c;
  color: white;
}
</style>

  