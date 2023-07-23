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
            box1: "flex w-16 h-12 m-auto justify-center items-center rounded-xl shadow-md shadow-black relative hover:scale-95 active:scale-105 ease-in-out duration-300",
            box13: "flex w-16 h-12 m-2.5 justify-center items-center rounded-xl bg-emerald-900 shadow-md shadow-black relative hover:scale-95 active:scale-105 ease-in-out duration-300",
            box2: "flex w-36 h-12 my-auto mx-1.5 justify-center items-center bg-gradient-to-r from-sky-500 to-indigo-500 rounded-xl shadow-md shadow-black relative hover:scale-95 active:scale-105 ease-in-out duration-300",
            box4: "flex w-16 h-12 m-2 justify-center items-center rounded-xl bg-emerald-400 shadow-md shadow-black relative hover:scale-95 active:scale-105 ease-in-out duration-300",
            
            btnNum: "w-full h-full text-3xl cursor-pointer text-white",
            btnFunc: "w-full h-full text-3xl cursor-pointer text-white",
            btnCount: "w-full h-full text-3xl cursor-pointer text-slate-400",
        }
    },
    mounted() {
        document.addEventListener('keydown', this.handleWatchEnter);
    },
    methods: {
        // number functions
        numfunction(num){
            
            if(this.resultshowup.includes("+")){
                this.includestype(num, "+");
                return;
            }
            else if(this.resultshowup.includes("x")){
                this.includestype(num, "x");
                return;
            }
            else if(this.resultshowup.includes("/")){
                this.includestype(num, "/");
                return;
            }
            else if(this.resultshowup.includes("-")){  
                this.includestype(num, "-");
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

        // count functions(call)
        numflagtype(buttontype){

            if(this.flagplus)
                this.flagtypedo("+",buttontype);
            else if(this.flagminus)
                this.flagtypedo("-",buttontype);
            else if(this.flagmulti)
                this.flagtypedo("x",buttontype);
            else if(this.flagdivided)
                this.flagtypedo("/",buttontype);
            else
                this.flagtypeshow(buttontype);
            

            this.result2 = 0;
            this.resultshow = "0";
            this.resultshowfix = "0";

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

        // others functions
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
            if(this.flagplus || this.flagminus || this.flagmulti || this.flagdivided){
                // console.log(this.resultshowfix);
                if((this.resultshow[this.resultshow.length - 2] === ".") || (this.resultshow[this.resultshow.length - 2] === "0")){
                    this.resultshow = this.resultshow.substring(0, this.resultshow.length - 1)
                    this.resultshowfix = this.resultshow;
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
                // console.log("1234");
                return;
            }
            if((this.resultshow[this.resultshow.length - 2] === ".") || (this.resultshow[this.resultshow.length - 2] === "0")){
                this.resultshow = this.resultshow.substring(0, this.resultshow.length - 1)
                this.resultshowup = "";
                this.resultshowfix = this.resultshow;
                // console.log("123123");
                return;
            }
            if(this.resultshow[this.resultshow.length - 1] === "."){
                this.flagdot = false;
            }
            this.result = +(this.resultshow.substring(0, this.resultshow.length - 1));
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            // console.log(this.resultshowfix);
            // for(let i=3;i<this.resultshowfix.length;i+=4){
            //     this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            // }
            this.resultshowup = "";
                
        },

        // number includes function
        includestype(num, type){
            
            if(type === "+")
                this.flagplus = true;
            if(type === "-")
                this.flagminus = true;
            if(type === "x")
                this.flagmulti = true;
            if(type === "/")
                this.flagdivided = true;

            if(this.resultshow.split('.').length - 1){
                // console.log("1: "+this.result2);
                if(num !== 0){
                    this.result2 = +(this.resultshow+num.toString());
                    this.resultshow = this.result2.toString();
                }
                else{
                    this.resultshow = this.resultshow+num.toString();
                }
                this.resultshowfix = this.resultshow;
                return;
            };
            // console.log("2: "+this.result2);
            this.result2 = this.result2*10 + +num;
            // console.log("2: "+this.result2);
            this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
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

        // count functions
        flagtypedo(flagtypebefore, flagtypeafter){
            let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
            let pownum2 = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) + ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
            
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
            
            if((flagtypebefore === "+") || (flagtypebefore === "-") || (flagtypebefore === "/"))
                this.result = Math.round(this.result * Math.pow(10, pownum+1)) / Math.pow(10, pownum+1);
            else if(flagtypebefore === "x")
                this.result = Math.round(this.result * Math.pow(10, pownum2+1)) / Math.pow(10, pownum2+1);
            
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
        },
        flagtypeshow(flagtype){
            this.flagdot = false;
            this.resultshowup = this.result.toString();

            if(flagtype === "+")
                this.resultshowup += "+";
            if(flagtype === "-")
                this.resultshowup += "-";
            if(flagtype === "x")
                this.resultshowup += "x";
            if(flagtype === "/")
                this.resultshowup += "/";
        },

        // keyboard input function
        handleWatchEnter(e){
            let key = window.Event ? e.keyCode : e.which;
            // console.log(key);
            if(key === 97)
                this.numfunction(1);
            else if(key === 98)
                this.numfunction(2);
            else if(key === 99)
                this.numfunction(3);
            else if(key === 100)
                this.numfunction(4);
            else if(key === 101)
                this.numfunction(5);
            else if(key === 102)
                this.numfunction(6);
            else if(key === 103)
                this.numfunction(7);
            else if(key === 104)
                this.numfunction(8);
            else if(key === 105)
                this.numfunction(9);
            else if(key === 96)
                this.numfunction(0);
            else if(key === 110)
                this.numdot();
            else if(key === 111)
                this.numflagtype('/');
            else if(key === 106)
                this.numflagtype('x');
            else if(key === 109)
                this.numflagtype('-');
            else if(key === 107)
                this.numflagtype('+');
            else if(key === 13)
                this.numflagtype('=');
            else if(key === 8)
                this.numback();
            else if(key === 46)
                this.numac();
        },
    },
}
</script>

<template>
    <body @keyup.enter=clickEnter() class="flex w-full h-screen m-auto justify-center items-center bg-black relative">
        <div class="w-80 h-5/6 rounded-2xl bg-cyan-700 relative">

            <div class="flex w-full h-1/5 rounded-t-2xl bg-cyan-950 relative">
                <p class="text-xl text-white absolute top-0.5 right-8">{{ resultshowup }}</p>
                <p class="text-6xl text-white absolute top-5 right-8">{{ resultshowfix }}</p>
            </div>

            <div class="h-5/6 relative m-auto justify-center items-center">
                <div :class=area>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(7)">7</button></div>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(8)">8</button></div>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(9)">9</button></div>
                    <div :class=box13><button type="button" :class=btnCount @click="numflagtype('/')">/</button></div>
                </div>
                <div :class=area>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(4)">4</button></div>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(5)">5</button></div>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(6)">6</button></div>
                    <div :class=box13><button type="button" :class=btnCount @click="numflagtype('x')">x</button></div>
                </div>
                <div :class=area>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(1)">1</button></div>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(2)">2</button></div>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(3)">3</button></div>
                    <div :class=box13><button type="button" :class=btnCount @click="numflagtype('+')">+</button></div>
                </div> 
                <div :class=area>
                    <div :class=box1><button type="button" :class=btnNum @click="numfunction(0)">0</button></div>
                    <div :class=box1><button type="button" :class=btnNum @click="num00()">00</button></div>
                    <div :class=box1><button type="button" :class=btnNum @click="numdot()">.</button></div>
                    <div :class=box13><button type="button" :class=btnCount @click="numflagtype('-')">-</button></div>
                </div>
                <div :class=area>
                    <div :class=box4><button type="button" :class=btnFunc @click="numac()">AC</button></div>
                    <div :class=box4><button type="button" :class=btnFunc @click="numback()">D</button></div>
                    <div :class=box2><button type="button" :class=btnNum @click="numequal()">=</button></div>
                </div>
            </div>

        </div>
    </body>
</template>

<style>
</style>