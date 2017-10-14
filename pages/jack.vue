<template>
        <section class="container">
          <div>
            <center>
                <div id="head">
                    <h1> Create</h1>
                </div>
                <div class="picter">
                  <table   style="width:100%;">
                    <tr>
                      <td style="width:25%;" id="pic"><img src="../assets/case.jpg" alt="" 
                        >
                        </td>
                        <td style="width:25%;" id="pic"><img src="../assets/case.jpg" alt="" 
                          >
                        </td>
                        <td style="width:25%;" id="pic"><img src="../assets/case.jpg" alt="" 
                          >
                        </td>
                        <td style="width:25%;"id="pic" ><img src="../assets/case.jpg" alt="" 
                          >
                        </td>
                    </tr>
                    <TR id="button">
                      <td><button>$1</button></td>
                      <td><button>$3</button></td>
                      <td><button>$6</button></td>
                      <td><button>$11</button></td>
                    </TR>
                </table>
                </div>
            </center>
          </div>
        </section>
      </template>
      
      <script>
        export default {
        
        }
      </script>
      
      <style>
        body{
          background: black;
        }
        #button > td >button{
          width: 80%;
          height: 30px;
          background:chartreuse;
          border:2px solid rgb(72, 255, 0);
          -webkit-border-radius:10px;
          -moz-border-radius:10px;
          margin-left: 10%;
        }
        #head{
           font-size: 50px;
           margin-top:20px;
           color: chartreuse;
         }
         .picter{
           margin-top:40px;
         }
         .container1{
           background: cadetblue;
         }
         #pic > img{
          -webkit-border-radius:10px;
          -moz-border-radius:10px;
            width: 80%;
            margin-left: 10%;
            height: 100%;
         }
      </style>
      