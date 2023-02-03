<template>

<div class="container">

  <div class="fixed_box">
    <h2>Category</h2>
   
    <div class="category">
       <li><span><input type="checkbox" name="chack" id=""></span>All</li>
        <li><span><input type="checkbox" name="chack" id=""></span>Payments</li>
        <li><span><input type="checkbox" name="chack" id=""></span>NonPayments</li>
        <li><span><input type="checkbox" name="chack" id=""></span>Programming</li>
        <li><span><input type="checkbox" name="chack" id=""></span>Arabic</li>
        <li><span><input type="checkbox" name="chack" id=""></span>English</li>
        <li><span><input type="checkbox" name="chack" id=""></span>Korea</li>
        <li><span><input type="checkbox" name="chack" id=""></span>Russian</li>
        <li><span><input type="checkbox" name="chack" id=""></span>History</li>
        <li><span><input type="checkbox" name="chack" id=""></span>Math</li>
        <!-- <ul v-for="(item, index) in categoryList " :key="index" class="typesbox">
            <li>
              <span><input type="checkbox" name="chack" id=""></span>
              {{item.category}}
            </li>
        </ul> -->
 
    </div>

      <ul class="addtitle">
       
        <li class="setting"><span><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" style="fill: rgba(0, 0, 0, 1);transform: ;msFilter:;"><path d="m2.344 15.271 2 3.46a1 1 0 0 0 1.366.365l1.396-.806c.58.457 1.221.832 1.895 1.112V21a1 1 0 0 0 1 1h4a1 1 0 0 0 1-1v-1.598a8.094 8.094 0 0 0 1.895-1.112l1.396.806c.477.275 1.091.11 1.366-.365l2-3.46a1.004 1.004 0 0 0-.365-1.366l-1.372-.793a7.683 7.683 0 0 0-.002-2.224l1.372-.793c.476-.275.641-.89.365-1.366l-2-3.46a1 1 0 0 0-1.366-.365l-1.396.806A8.034 8.034 0 0 0 15 4.598V3a1 1 0 0 0-1-1h-4a1 1 0 0 0-1 1v1.598A8.094 8.094 0 0 0 7.105 5.71L5.71 4.904a.999.999 0 0 0-1.366.365l-2 3.46a1.004 1.004 0 0 0 .365 1.366l1.372.793a7.683 7.683 0 0 0 0 2.224l-1.372.793c-.476.275-.641.89-.365 1.366zM12 8c2.206 0 4 1.794 4 4s-1.794 4-4 4-4-1.794-4-4 1.794-4 4-4z"></path></svg></span> Settings</li>
      </ul>

  </div>


  

    <div class="todobox">
      <div class="box">
        <h1>ToDo App Education</h1>
          <!-- <ul class="items">
             <li><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" style="fill: rgba(0, 0, 0, 1);transform: ;msFilter:;"><path d="M4.5 8.552c0 1.995 1.505 3.5 3.5 3.5s3.5-1.505 3.5-3.5-1.505-3.5-3.5-3.5-3.5 1.505-3.5 3.5zM19 8h-2v3h-3v2h3v3h2v-3h3v-2h-3zM4 19h10v-1c0-2.757-2.243-5-5-5H7c-2.757 0-5 2.243-5 5v1h2z"></path></svg></li>
            
            <input v-model.trim="value" class="npt" type="text" placeholder="Enter Students">
            <button v-if="currentId === null" @click.enter="addMale" class="add">Add Male</button>
            <button v-if="currentId === null" @click.enter="addFemale" class="add">Add Female</button>
              <button v-else @click.enter="renameTodo" class="add">Rename</button>
          </ul>  -->
          <ul class="items">
            <li><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" style="fill: rgba(0, 0, 0, 1);transform: scaleX(-1);msFilter:progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);"><path d="M10 18a7.952 7.952 0 0 0 4.897-1.688l4.396 4.396 1.414-1.414-4.396-4.396A7.952 7.952 0 0 0 18 10c0-4.411-3.589-8-8-8s-8 3.589-8 8 3.589 8 8 8zm0-14c3.309 0 6 2.691 6 6s-2.691 6-6 6-6-2.691-6-6 2.691-6 6-6z"></path><path d="M11.412 8.586c.379.38.588.882.588 1.414h2a3.977 3.977 0 0 0-1.174-2.828c-1.514-1.512-4.139-1.512-5.652 0l1.412 1.416c.76-.758 2.07-.756 2.826-.002z"></path></svg></li>
            <input class="npt" type="search" name="" id="">
          </ul>
          <ul>
             <li></li>
          </ul>
          </div>



          <div class="list_box">
            <div class="added"  v-for="(item, intg) in todoList" :key="intg">
             <div>
               <span>{{intg + 1 +'. '}}</span>
               <span>{{item.title}}</span>
               <span>{{item.subject}}</span>
             </div>
               

              <div class="btn">
                 <span>{{item.tell}}</span>
                 <button @click="removeItem(item)">Delete</button>
                 <button @click="renameItem(item)">Rename</button>
              
                <div>
                  <label for="pay">Payment</label>
                 <span> <input type="checkbox"></span>
                 
              </div>
            </div>
          </div>
          
      </div>
    
  
      
      <div class="addin">
        <form id="todoadd" @submit.prevent="addTodo">
          <label for="fname">FullName</label><br>
          <input placeholder="Abdufattoyev Shahboz" type="text" v-model.trim="fname" name="fname"><br>
        <label for="tel">Tel number</label><br>
          <input placeholder="Tel:932987668" type="tell" v-model.trim="tell" name="tell"><br>
          <label for="subj">Subject</label><br> 
          <input placeholder="Frontend" type="text" v-model.trim="subject" name="subj"> <br>
          <label for="category">Category</label><br>
         <select name="select" id="">
            <option value="programming">Programming</option>
            <option value="arabic">Arabic</option>
            <option value="english">English</option>
            <option value="korean">Korean</option>
            <option value="russian">Russian</option>
            <option value="math">MAth</option>
            <option value="history">History</option>
            <option value="individual">Individual</option>
          </select><br><br>
         <input type="submit" value="submit">
        </form>
      </div>
      
</div>

</template>


<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      // newCategory:'',
      // male:'',
      // female: '',
      // categoryList: [],
      fname:'',
      idCreater: 0,
      todoList: [],
      currentId: null,
      tell:null,
      subject: '',
      category:''
    }
  },
  mounted(){
    // this.idCreater = this.todoList.length
  },
  methods: {
      addTodo(){
      // if(this.fname.length)
      
          this.idCreater++,
          this.todoList.push({
          id: this.idCreater,
          title: this.fname,
          tell: this.tell,
          category: this.category
      })
       this.fname = ''
    console.log(this.todoList)
    },
    },
      removeItem(item){
      const intg = this.todoList.findIndex( el => el.id  === item.id )
      this.todoList.splice(intg, 1)
   },
    renameItem(item) {
      this.fname = item.title
      this.currentId = item.id
   },
      renameTodo() {
        const index = this.todoList.findIndex( el => el.id  === this.currentId )
        this.todoList[index].title = this.value
        this.currentId = this.value = null
    },
   
  }

</script>


<style scoped>
*{
  list-style: none;
}
.container{
  width: 1300px;
  display: flex;
 justify-content: space-between;
}
 
.category{
  scroll-behavior:smooth;
  max-height: 400px;
   overflow: hidden;
  
}
.category li{
  margin-top: 10px;
  font-size: 20px;
}
 .setting{
  text-decoration: underline #171616 2px dotted;
  display:flex;
  align-items: center;
 }

.fixed_box{
  width: 250px;
   height: 800px;
  position: fixed;
 margin: -10px 0;
  /* border-right: solid 1px #232323; */
    background-color: aqua;
 padding:100px 20px;
 box-shadow: blueviolet 1px 1px 5px;
 z-index: 111;
}
.typesbox{
position: relative;
}
.typesbox li{
  font-size: 20px;
}
.addtitle{
  position: absolute;
 top: 500px;
  cursor: pointer;
}
.addtitle li{
  opacity: 0.8;
font-size: 20px;
 margin-top: 10px;
}
.box{
  padding-top: 0;
  position: fixed;
  top: 0;
  left: 300px;
  width: 54%;
  background-color: aqua;
border:1px solid blueviolet ;
z-index: 121;
}
#pay{
  display: flex;
}
.added{
  border-bottom: #232323 1px solid;
  margin-top: 10px;
  display: flex;
   align-items: center;
   justify-content: space-around;
   align-items: flex-end;
}
.addin{
  position: fixed;
  /* flex-direction: column; */
  padding-left:25px;
  width: 300px;
  margin-top: -10px;
  right: 0;
  height: 800px;
  background-color: aqua;
 
}
#todoadd{
  margin-top: 100px;
}
#todoadd input{
  width: 250px;
  height: 25px;
  margin-bottom: 50px;
}
h1{
  text-align: center;
  color: blue;
}
.todobox{
width: 70%;
height:150px;
 margin-left: auto;
margin-top: 100px;
}
.items{
  display: flex;
  align-items: center;
  list-style: none;
  gap: 10px;
}
.btn{
  width: 200px;
  display: flex;
  justify-content: space-evenly;
  align-items:center;
}
.npt{
  padding:5px;
  width: 500px;
  border-radius: 5px;
outline:none;
border:1px solid blueviolet ;
font-size: 20px;
}
.list_box{
 width:78%;
 margin-top: 100px;
position: relative;
left:-80px;
font-size: 20px;
}
.add{
  width: 130px;
  height: 35px;
  background: none;
  border: none;
  font-size: 15px;
cursor: pointer;
}
.add:hover{
  background-color: rgb(148, 148, 176);
  color: blue;
}

</style>