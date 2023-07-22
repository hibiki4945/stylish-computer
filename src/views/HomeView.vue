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
            box2: "flex w-64 h-12 my-auto mx-2.5 justify-center items-center bg-gradient-to-r from-sky-500 to-indigo-500 rounded-xl",
            box13: "flex w-24 h-12 m-2.5 justify-center items-center rounded-xl bg-emerald-900",
            box4: "flex w-24 h-12 m-2.5 justify-center items-center rounded-xl bg-emerald-400",
            
            btnNum: "text-3xl cursor-pointer text-white",
            btnFunc: "text-3xl cursor-pointer text-white",
            btnCount: "text-3xl cursor-pointer text-slate-400",
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
        flagtypeshow(flagtype){
            this.resultshow = "0";
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