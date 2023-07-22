<script>
export default {
    data() {
        return {
            result: 0,
            result2: 0,
            resultshowup: "",
            resultshow: "0",
            resultshowupfix: "",
            resultshowfix: "0",
            flagplus: false,
            flagminus: false,
            flagmulti: false,
            flagdivided: false,
            flagdot: false,
            area: "flex",
            box1: "flex w-24 h-12 m-auto justify-center items-center rounded-xl",
            box2: "flex w-52 h-12 my-auto mx-2 justify-center items-center bg-gradient-to-r from-sky-500 to-indigo-500 rounded-xl",
            box13: "flex w-24 h-12 m-2.5 justify-center items-center rounded-xl bg-emerald-900",

        }
    },
    methods: {
        numfunction(num){
            if(this.resultshowup.includes("+")){
                this.flagplus = true;
                this.includesplus(num);
                return;
            }
            else if(this.resultshowup.includes("x")){
                this.flagmulti = true;
                this.includesmulti(num);
                return;
            }
            else if(this.resultshowup.includes("/")){
                this.flagdivided = true;
                this.includesdivided(num);
                return;
            }
            else if(this.resultshowup.includes("-")){
                this.flagminus = true;
                this.includesminus(num);
                return;
            }
            if(this.resultshow.includes(".")){
                this.includesdot(num);
                return;
            };
            this.result = this.result*10 + +num;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
        },
        num00(){
            this.numfunction(0);
            this.numfunction(0);
        },

        numplus(){
            if(this.flagplus)
                this.flagtypedo("+","+");
            else if(this.flagminus)
                this.flagtypedo("-","+");
            else if(this.flagmulti)
                this.flagtypedo("x","+");
            else if(this.flagdivided)
                this.flagtypedo("/","+");
            else{
                this.resultshow = "0";
                this.flagdot = false;
                this.resultshowup = this.result.toString();
                this.resultshowup += "+";
            }
            this.result2 = 0;

        },
        numminus(){
            if(this.flagplus)
                this.flagtypedo("+","-");
            else if(this.flagminus)
                this.flagtypedo("-","-");
            else if(this.flagmulti)
                this.flagtypedo("x","-");
            else if(this.flagdivided)
                this.flagtypedo("/","-");
            else{
                this.resultshow = "0";
                this.flagdot = false;
                this.resultshowup = this.result.toString();
                this.resultshowup += "-";
            }
            this.result2 = 0;

        },
        nummulti(){
            if(this.flagplus)
                this.flagtypedo("+","x");
            else if(this.flagminus)
                this.flagtypedo("-","x");
            else if(this.flagmulti)
                this.flagtypedo("x","x");
            else if(this.flagdivided)
                this.flagtypedo("/","x");
            else{
                this.resultshow = "0";
                this.flagdot = false;
                this.resultshowup = this.result.toString();
                this.resultshowup += "x";
            }
            this.result2 = 0;

        },
        numdivided(){
            if(this.flagplus)
                this.flagtypedo("+","/");
            else if(this.flagminus)
                this.flagtypedo("-","/");
            else if(this.flagmulti)
                this.flagtypedo("x","/");
            else if(this.flagdivided)
                this.flagtypedo("/","/");
            else{
                this.resultshow = "0";
                this.flagdot = false;
                this.resultshowup = this.result.toString();
                this.resultshowup += "/";
            }
            this.result2 = 0;

        },
        numequal(){
            if(this.flagplus)
                this.flagtypedo("+","=");
            else if(this.flagminus)
                this.flagtypedo("-","=");
            else if(this.flagmulti)
                this.flagtypedo("x","=");
            else if(this.flagdivided)
                this.flagtypedo("/","=");
                
            this.result2 = 0;
           
        },

        numdot(){
            
            if(this.flagdot){
                return;
            }

            this.flagdot = true;
            this.resultshow += ".";
            this.resultshowfix = this.resultshow;
        },
        numac(){
            this.result = 0;
            this.result2 = 0;
            this.resultshowup = "";
            this.resultshow = "0";
            this.resultshowupfix = "";
            this.resultshowfix = "0";

            this.flagplus = false;
            this.flagminus = false;
            this.flagmulti = false;
            this.flagdivided = false;
            this.flagdot = false;

        },
        numback(){
            
            // console.log("resultshow:"+this.resultshow);
            // console.log("resultshowup:"+this.resultshowup);

            if(this.resultshowup.includes("+")){

                if((this.resultshow[this.resultshow.length - 2] === ".") || (this.resultshow[this.resultshow.length - 2] === "0")){
                    // console.log("lastdot!");
                    this.resultshow = this.resultshow.substring(0, this.resultshow.length - 1)
                    this.resultshowup = this.resultshow;
                    return;
                }
                if(this.resultshow[this.resultshow.length - 1] === "."){
                    this.flagdot = false;
                }
                this.result2 = +(this.resultshow.substring(0, this.resultshow.length - 1));
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
                // this.resultshowup = this.resultshow;
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log("flagminus!");
                this.flagminus = true;
                this.result2 = Math.floor(this.result2/10);
                this.resultshow += this.result2.toString();
                return;
            }
            if((this.resultshow[this.resultshow.length - 2] === ".") || (this.resultshow[this.resultshow.length - 2] === "0")){
                // console.log("lastdot!");
                this.resultshow = this.resultshow.substring(0, this.resultshow.length - 1)
                this.resultshowup = this.resultshow;
                return;
            }
            if(this.resultshow[this.resultshow.length - 1] === "."){
                this.flagdot = false;
            }
            this.result = +(this.resultshow.substring(0, this.resultshow.length - 1));
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
            this.resultshowup = this.resultshow;
                
        },

        includesplus(num){

            if(this.resultshow.split('.').length - 1){
                this.flagplus = true;
                this.result2 = +(this.resultshow+num.toString());
                this.resultshow = this.result2.toString();
                this.resultshowfix = this.resultshow;
                // for(let i=3;i<this.resultshowfix.length;i+=4){
                //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
                // }
                return;
            };
            this.flagplus = true;
            this.result2 = this.result2*10 + +num;
            this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
        },
        includesminus(num){
            if(this.resultshow.split('.').length - 1){
                this.result2 = +(this.resultshow+num.toString());
                this.resultshow = this.result2.toString();
                this.resultshowfix = this.resultshow;
                // for(let i=3;i<this.resultshowfix.length;i+=4){
                //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
                // }
                return;
            };
            this.result2 = this.result2*10 + +num;
            this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
        },
        includesmulti(num){
            if(this.resultshow.split('.').length - 1){
                this.resultshow = this.resultshow+num.toString();
                return;
            };
            this.result2 = this.result2*10 + +num;
            this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
        },
        includesdivided(num){
            if(this.resultshow.split('.').length - 1){
                this.resultshow = this.resultshow+num.toString();
                return;
            };
            this.result2 = this.result2*10 + +num;
            this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            // this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
        },
        includesdot(num){
            if(num !== 0){
                this.resultshow += num.toString()
                this.result = +(this.resultshow);
            }
            else{
                this.resultshow += num.toString();
            }
            this.resultshowfix = this.resultshow;
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
        },

        flagtypedo(flagtypebefore, flagtypeafter){
            let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
            pownum++;
            this.flagplus = false;
            this.flagminus = false;
            this.flagmulti = false;
            this.flagdivided = false;

            if(flagtypebefore === "+")
                this.result += this.result2;
            else if(flagtypebefore === "-")
                this.result -= this.result2;
            else if(flagtypebefore === "x")
                this.result *= this.result2;
            else if(flagtypebefore === "/")
                this.result /= this.result2;
            
            if((flagtypebefore === "+") || (flagtypebefore === "-"))
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
            
            if(flagtypeafter === "+")
                this.resultshowup = this.result+"+";
            else if(flagtypeafter === "-")
                this.resultshowup = this.result+"-";
            else if(flagtypeafter === "x")
                this.resultshowup = this.result+"x";
            else if(flagtypeafter === "/")
                this.resultshowup = this.result+"/";
            else if(flagtypeafter === "=")
                this.resultshowup = this.result;

            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
        },
    },
}
</script>

<template>
    <body class="flex w-full h-screen m-auto justify-center items-center bg-black relative">
        <div class="w-80 h-5/6 rounded-2xl bg-cyan-700 relative">

            <div class="flex w-full h-1/5 rounded-t-2xl bg-cyan-950 relative">
                <p class="text-xl text-white absolute top-0.5 right-8">{{ resultshowup }}</p>
                <p class="text-6xl text-white absolute top-5 right-8">{{ resultshowfix }}</p>
            </div>

            <div class="h-5/6 relative m-auto justify-center items-center">
                <div :class=area>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(7)">7</button></div>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(8)">8</button></div>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(9)">9</button></div>
                    <div :class=box13><button type="button" class="btn btn-func btn-count" @click="numdivided()">/</button></div>
                </div>
                <div :class=area>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(4)">4</button></div>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(5)">5</button></div>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(6)">6</button></div>
                    <div :class=box13><button type="button" class="btn btn-func btn-count" @click="nummulti()">x</button></div>
                </div>
                <div :class=area>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(1)">1</button></div>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(2)">2</button></div>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(3)">3</button></div>
                    <div :class=box13><button type="button" class="btn btn-func btn-count" @click="numplus()">+</button></div>
                </div> 
                <div :class=area>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numfunction(0)">0</button></div>
                    <div :class=box1><button type="button" class="btn btn-num" @click="num00()">00</button></div>
                    <div :class=box1><button type="button" class="btn btn-num" @click="numdot()">.</button></div>
                    <div :class=box13><button type="button" class="btn btn-func btn-count" @click="numminus()">-</button></div>
                </div>
                <div :class=area>
                    <div :class=box1><button type="button" class="btn btn-func" @click="numac()">AC</button></div>
                    <div :class=box1><button type="button" class="btn btn-func" @click="numback()">D</button></div>
                    <div :class=box2><button type="button" class="btn btn-num btn-equal" @click="numequal()">=</button></div>
                </div>
            </div>

        </div>
    </body>
</template>

<style lang="scss" scoped>
    // .container{
    //     width: 300px;
    //     height: 450px;
    //     border-radius: 20px;
    //     background-color: #2f3dd5;
    //     position: relative;

    //     .result-area{
    //         display: flex;
    //         width: 100%;
    //         height: 20%;
    //         border-top-left-radius: 20px;
    //         border-top-right-radius: 20px;
    //         background-color: #0b1363;
    //         position: relative;

    //         .p1{
    //             font-size: 20px;
    //             color: white;
    //             position: absolute;
    //             top: 10px;
    //             right: 30px;
    //         }
    //         p{
    //             font-size: 60px;
    //             color: white;
    //             position: absolute;
    //             top: 20px;
    //             right: 30px;
    //         }
    //     }
    //     .button-area{
    //         height: 80%;
    //         position: relative;
    //         margin: auto;
    //         justify-content: center;
    //         align-items: center;
    //         .area{
    //             display: flex;
    //             .box1{
    //                 display: flex;
    //                 width: 100px;
    //                 height: 50px;
    //                 margin: auto;
    //                 justify-content: center;
    //                 align-items: center;
    //                 border-radius: 10px;
    //             }
    //             .box2{
    //                 display: flex;
    //                 width: 200px;
    //                 height: 50px;
    //                 margin: auto 10px;
    //                 justify-content: center;
    //                 align-items: center;
    //                 background: linear-gradient(to right,  rgb(66, 202, 223), rgb(171, 67, 212));
    //                 border-radius: 10px;
    //             }
    //             .box3{
    //                 margin: 10px;
    //                 background-color: #111972;
    //                 border-radius: 10px;
    //             }
    //         }
    //         .btn{
    //             font-size: 30px;
    //             background-color: #2f3dd5;
    //             cursor: pointer;
    //         }
    //         .btn-num{
    //             color: white;
    //         }
    //         .btn-func{
    //             color: #9399e0;
    //         }
    //         .btn-count{
    //             background-color: #111972;
    //         }
    //         .btn-equal{
    //             width: 100px;
    //             background:none;
    //         }
    //     }
    // }
</style>