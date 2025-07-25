<template>
    <div class="container">
        <form>
            <div class="form-group">
            <label>Email Address:</label>
            <input type="email" placeholder="example@email.com" required v-model="email">

            <label>Password:</label>
            <input type="password" placeholder="Password" required v-model="password">
            <label>Role</label>
            <select v-model="role">
                <option value="Developer">Web Develop</option>
                <option value="Designer">Web Design</option>
            </select>
                <label>Skills</label>
                <input type="text" v-model="tempSkill" @keyup="addSkill">
                <div class="d-flex gap-1">
                    <div v-for="skill in skills" :key="skill" class="pill">
                    <span @click="deleteSkill(skill)">{{ skill }}</span>
                </div>
                </div>
            <div class="terms">
                <input type="checkbox" v-model="terms" required>
                <label>Accept terms and conditions</label>
            </div>

            </div>
            <button type="submit" class="rounded-1">Submit</button>
        </form>

        <p>Email : {{ email }}</p>
        <p>Password : {{ password }}</p>
        <p>Role : {{ role }}</p>
        <p>term : {{ terms }}</p>

    </div>
</template>

<script>
    import { defineComponent, ref } from 'vue';


export default defineComponent({
    
  data() {
    const email = ref('');
    const password = ref('');
    const role = ref('');
    const terms = ref('');
    const tempSkill = ref();
    // const skills = ref ();
    return { email,
            password,
            role,
            terms,
            tempSkill,
            skills: []
          }
  },
  methods: {
    
    addSkill(e) {
        if(e.key === ',' && this.tempSkill){
            if(!this.skills.includes(this.tempSkill)){
                this.skills.push(this.tempSkill)  
            }
            this.tempSkill = ''
        } 
            
    }
  },
  deleteSkill(skill){
    this.skills = this.skills.filter((item) => {
        return skill !== item
    })
  }
});
</script>

<style>
    form {
      background-color: #fff;
      max-width: 400px;
      margin: auto;
      padding: 2rem;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .form-group {
      display: flex;
      flex-direction: column;
      margin-bottom: 1.5rem;
    }

    label {
      font-weight: 600;
      margin: 0.5rem 0px;
      color: #333;
    }

    input,select{
      padding: 0.6rem 1rem;
      font-size: 1rem;
      border: 1px solid #ccc;
      border-radius: 8px;
      transition: border-color 0.3s;
    }

    input:focus {
      border-color: #007BFF;
      outline: none;
      box-shadow: 0 0 4px rgba(0, 123, 255, 0.3);
    }

    button {
      background-color: #007BFF;
      color: white;
      padding: 0.6rem 1.2rem;
      font-size: 1rem;
      border: none;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #0056b3;
    }

    input[type="checkbox"]{
        display: inline-block;
        width: 16px;
        margin-right: 5px;
    }
    .pill{
        display: inline-block;
        margin: 20px 10px 0 0;
        padding: 6px 12px;
        background: #eee;
        border-radius: 20px;
        font-size: 12px;
        letter-spacing: 1;
        font-weight: bold;
        color: #777;
        cursor: pointer;

    }
</style>