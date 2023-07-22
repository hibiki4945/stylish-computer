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
        }
    },
    methods: {
        num0(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.resultshow = this.resultshow+"0";
                    // this.result = +(this.resultshow+"0");
                    // this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 0;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                if(this.resultshow.split('.').length - 1){
                    this.flagminus = true;
                    this.resultshow = this.resultshow+"0";
                    return;
                };
                this.flagminus = true;
                this.result2 = this.result2*10 + 0;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"0";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 0;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"0";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 0;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }

  
            // console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.resultshow = this.resultshow+"0";
                    // this.result = +(this.resultshow+"0");
                    // this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 0;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num00(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.resultshow = this.resultshow+"00";
                    // this.result = +(this.resultshow+"0");
                    // this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*100 + 0;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagminus = true;
                    // this.result /= 10;
                    this.resultshow = this.resultshow+"00";
                    // this.result = +(this.resultshow+"0");
                    // this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagminus = true;
                this.result2 = this.result2*100 + 0;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"00";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 0;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"00";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 0;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            // console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.resultshow = this.resultshow+"00";
                    // this.result = +(this.resultshow+"0");
                    // this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*100 + 0;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num1(){
            if(this.resultshowup.includes("+")){
                this.flagplus = true;
                this.includesplus(1);
                return;
            }
            else if(this.resultshowup.includes("-")){
                if(this.resultshow.split('.').length - 1){
                    this.flagminus = true;
                    this.result2 = +(this.resultshow+"1");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                this.flagminus = true;
                this.result2 = this.result2*10 + 1;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"1";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 1;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"1";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 1;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            if(this.resultshow.includes(".")){
                    this.result = +(this.resultshow+"1");
                    this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 1;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num2(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"2");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 2;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagminus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"2");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagminus = true;
                this.result2 = this.result2*10 + 2;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"2";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 2;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"2";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 2;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.result = +(this.resultshow+"2");
                    this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 2;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num3(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"3");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 3;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagminus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"3");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagminus = true;
                this.result2 = this.result2*10 + 3;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"3";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 3;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"3";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 3;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            // console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.result = +(this.resultshow+"3");
                    this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 3;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num4(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"4");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 4;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagminus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"4");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagminus = true;
                this.result2 = this.result2*10 + 4;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"4";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 4;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"4";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 4;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            // console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.result = +(this.resultshow+"4");
                    this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 4;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num5(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"5");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 5;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagminus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"5");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagminus = true;
                this.result2 = this.result2*10 + 5;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"5";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 5;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"5";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 5;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            // console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.result = +(this.resultshow+"5");
                    this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 5;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num6(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"6");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 6;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagminus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"6");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagminus = true;
                this.result2 = this.result2*10 + 6;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"6";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 6;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"6";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 6;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            // console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.result = +(this.resultshow+"6");
                    this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 6;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num7(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"7");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 7;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagminus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"7");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagminus = true;
                this.result2 = this.result2*10 + 7;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"7";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 7;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"7";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 7;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            // console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.result = +(this.resultshow+"7");
                    this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 7;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num8(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"8");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 8;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagminus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"8");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagminus = true;
                this.result2 = this.result2*10 + 8;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"8";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 8;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"8";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 8;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            // console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.result = +(this.resultshow+"8");
                    this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 8;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        num9(){
            if(this.resultshowup.includes("+")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"9");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 9;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("-")){
                // console.log((this.resultshowup.split('.').length - 1));
                // console.log((this.resultshowup.split('.').length - 1) >= 2);
                if(this.resultshow.split('.').length - 1){
                    // console.log("flagdot!");
                    // console.log("flagplus!");
                    this.flagplus = true;
                    // this.result /= 10;
                    this.result2 = +(this.resultshow+"9");
                    this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    
                    return;
                };
                // console.log("flagplus!");
                this.flagplus = true;
                this.result2 = this.result2*10 + 9;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("x")){
                if(this.resultshow.split('.').length - 1){
                    this.flagmulti = true;
                    this.resultshow = this.resultshow+"9";
                    return;
                };
                this.flagmulti = true;
                this.result2 = this.result2*10 + 9;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
            else if(this.resultshowup.includes("/")){
                if(this.resultshow.split('.').length - 1){
                    this.flagdivided = true;
                    this.resultshow = this.resultshow+"9";
                    return;
                };
                this.flagdivided = true;
                this.result2 = this.result2*10 + 9;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                return;
            }
  
            // console.log(this.resultshow);
            if(this.resultshow.includes(".")){
                    // console.log("flagdot!");
                    // this.result /= 10;
                    this.result = +(this.resultshow+"9");
                    this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
                    return;
                };
            this.result = this.result*10 + 9;
            this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        },
        numplus(){
            if(this.flagplus){
                let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
                pownum++;
                this.flagplus = false;
                // console.log("flagplus do!");
                this.result += this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                this.resultshowup = this.result+"+";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagminus){
                let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
                pownum++;
                this.flagminus = false;
                // console.log("flagminus do!");
                this.result -= this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                this.resultshowup = this.result+"+";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagmulti){
                this.flagmulti = false;
                // console.log("flagminus do!");
                this.result *= this.result2;
                this.resultshowup = this.result+"+";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagdivided){
                this.flagdivided = false;
                // console.log("flagminus do!");
                this.result /= this.result2;
                this.resultshowup = this.result+"+";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else{
                // this.flagplus = true;
                this.resultshow = "0";
                this.flagdot = false;
                this.resultshowup = this.result.toString();
                this.resultshowup += "+";
            }
            this.result2 = 0;

            // var str = "Hello world, welcome to the Runoob.";
            // var n = str.includes("world", 12);
            // console.log(n);

        },
        numminus(){
            if(this.flagplus){
                let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
                pownum++;
                this.flagplus = false;
                // console.log("flagplus do!");
                this.result += this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                this.resultshowup = this.result+"-";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagminus){
                let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
                pownum++;
                this.flagminus = false;
                // console.log("flagminus do!");
                this.result -= this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                this.resultshowup = this.result+"-";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagmulti){
                this.flagmulti = false;
                // console.log("flagminus do!");
                this.result *= this.result2;
                this.resultshowup = this.result+"-";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagdivided){
                this.flagdivided = false;
                // console.log("flagminus do!");
                this.result /= this.result2;
                this.resultshowup = this.result+"-";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else{
                // this.flagplus = true;
                this.resultshow = "0";
                this.flagdot = false;
                this.resultshowup = this.result.toString();
                this.resultshowup += "-";
            }
            this.result2 = 0;

            // var str = "Hello world, welcome to the Runoob.";
            // var n = str.includes("world", 12);
            // console.log(n);

        },
        nummulti(){
            if(this.flagplus){
                let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
                pownum++;
                this.flagplus = false;
                // console.log("flagplus do!");
                this.result += this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                this.resultshowup = this.result+"x";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagminus){
                let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
                pownum++;
                this.flagminus = false;
                // console.log("flagminus do!");
                this.result -= this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                this.resultshowup = this.result+"x";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagmulti){
                this.flagmulti = false;
                // console.log("flagminus do!");
                this.result *= this.result2;
                this.resultshowup = this.result+"x";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagdivided){
                this.flagdivided = false;
                // console.log("flagminus do!");
                this.result /= this.result2;
                this.resultshowup = this.result+"x";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else{
                // this.flagplus = true;
                this.resultshow = "0";
                this.flagdot = false;
                this.resultshowup = this.result.toString();
                this.resultshowup += "x";
            }
            this.result2 = 0;

            // var str = "Hello world, welcome to the Runoob.";
            // var n = str.includes("world", 12);
            // console.log(n);
        },
        numdivided(){
            if(this.flagplus){
                let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
                pownum++;
                this.flagplus = false;
                // console.log("flagplus do!");
                this.result += this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                this.resultshowup = this.result+"/";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagminus){
                let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
                pownum++;
                this.flagminus = false;
                // console.log("flagminus do!");
                this.result -= this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                this.resultshowup = this.result+"/";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagmulti){
                this.flagmulti = false;
                // console.log("flagminus do!");
                this.result *= this.result2;
                this.resultshowup = this.result+"/";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagdivided){
                this.flagdivided = false;
                // console.log("flagminus do!");
                this.result /= this.result2;
                this.resultshowup = this.result+"/";
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else{
                // this.flagplus = true;
                this.resultshow = "0";
                this.flagdot = false;
                this.resultshowup = this.result.toString();
                this.resultshowup += "/";
            }
            this.result2 = 0;

            // var str = "Hello world, welcome to the Runoob.";
            // var n = str.includes("world", 12);
            // console.log(n);
        },
        numequal(){
            // console.log("result:"+this.result);
            // console.log("result2:"+this.result2);
            // console.log("resultshow:"+this.resultshow);
            // console.log("resultshowup:"+this.resultshowup);
            // console.log("resultshow.length:"+this.resultshow.length);
            // console.log("resultshowup.length-1:"+(this.resultshowup.length-1));
            // console.log("resultshow.dot(index)+1:"+(this.resultshow.indexOf('.', 0)+1));
            // console.log("resultshowup.dot(index)+1:"+(this.resultshowup.indexOf('.', 0)+1));
            
            // console.log("resultshow.length - (resultshow.dot(index)+1):"+(this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)));
            // console.log("resultshowup.length-1 - (resultshowup.dot(index)+1):"+((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)));
            
            // console.log("resultshow's dot > resultshowup's dot:"+((this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1))));
            
            // console.log("resultshow's dot > resultshowup's dot ? resultshow's dot:resultshowup's -> "+((this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? 100:200));
            // console.log("resultshow's dot > resultshowup's dot ? resultshow's dot:resultshowup's -> "+((this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1))));
            
            let pownum = (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)) > ((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1)) ? (this.resultshow.length - (this.resultshow.indexOf('.', 0)+1)):((this.resultshowup.length-1) - (this.resultshowup.indexOf('.', 0)+1));
            pownum++;
            // 'Blue Whale'.indexOf('Whale', 0); 
            if(this.flagplus){
                this.flagplus = false;
                // console.log("flagplus do!");
                this.result += this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                // console.log("this.result + this.result2:"+this.result);
                this.resultshowup = this.result.toString();
                // console.log("resultshowup:"+this.resultshowup);
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagminus){
                this.flagminus = false;
                // console.log("flagminus do!");
                this.result -= this.result2;
                this.result = Math.round(this.result * Math.pow(10, pownum)) / Math.pow(10, pownum);
                // console.log("this.result + this.result2:"+this.result);
                this.resultshowup = this.result.toString();
                // console.log("resultshowup:"+this.resultshowup);
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagmulti){
                this.flagmulti = false;
                // console.log("flagminus do!");
                this.result *= this.result2;
                this.resultshowup = this.result.toString();
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            else if(this.flagdivided){
                this.flagdivided = false;
                // console.log("flagminus do!");
                this.result /= this.result2;
                this.resultshowup = this.result.toString();
                this.resultshow = this.result.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            }
            this.result2 = 0;
            // console.log("resultshow:"+this.resultshow);
            // console.log("resultshowup:"+this.resultshowup);
            
        },
        numdot(){
            
            if(this.flagdot){
                return;
            }

            this.flagdot = true;
            this.resultshow += ".";
        },
        numac(){
            // this.result = this.result*10 + 1;

            this.result = 0;
            this.result2 = 0;
            this.resultshowup = "";
            this.resultshow = "0";
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
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
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
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
            this.resultshowup = this.resultshow;
                
        },
        includesplus(num){

            if(this.resultshow.split('.').length - 1){
                    this.flagplus = true;
                    this.result2 = +(this.resultshow+num.toString());
                    this.resultshow = this.result2.toString();
                    this.resultshowfix = this.resultshow;
                    for(let i=3;i<this.resultshowfix.length;i+=4){
                        this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
                    }
                    
                    return;
                };
                this.flagplus = true;
                this.result2 = this.result2*10 + +num;
                this.resultshow = this.result2.toString();
            this.resultshowfix = this.resultshow;
            for(let i=3;i<this.resultshowfix.length;i+=4){
                this.resultshowfix = this.resultshowfix.slice(0, i) + "," + this.resultshowfix.slice(i);
            }
        }
    },
}
</script>

<template>
    <!-- <p>123</p>/ -->
    <div class="container">
        <div class="result-area">
            <p class="p1">{{ resultshowup }}</p>
            <!-- <p>{{ resultshow }}</p> -->
            <p class="p2">{{ resultshowfix }}</p>
            <p v-if="false">+</p>
        </div>

        <div class="button-area">
            <div class="area">
                <div class="box1">
                    <button type="button" class="btn btn-num" @click="num7()">7</button>
                </div>
                <div class="box1">
                    <button type="button" class="btn btn-num" @click="num8()">8</button>       
                </div>
                <div class="box1">
                    <button type="button" class="btn btn-num" @click="num9()">9</button>     
                </div>
                <div class="box1 box3">
                    <button type="button" class="btn btn-func btn-count" @click="numdivided()">/</button>
                </div>
            </div>
            <div class="area">
                <div class="box1"><button type="button" class="btn btn-num" @click="num4()">4</button>
                </div>
                <div class="box1"><button type="button" class="btn btn-num" @click="num5()">5</button>
                </div>
                <div class="box1"><button type="button" class="btn btn-num" @click="num6()">6</button>
                </div>
                <div class="box1 box3"><button type="button" class="btn btn-func btn-count" @click="nummulti()">x</button>
            </div>
            </div>
            <div class="area">
                <div class="box1"><button type="button" class="btn btn-num" @click="num1">1</button>
                </div>
                <div class="box1"><button type="button" class="btn btn-num" @click="num2()">2</button>
                </div>
                <div class="box1"><button type="button" class="btn btn-num" @click="num3()">3</button>
                </div>
                <div class="box1 box3"><button type="button" class="btn btn-func btn-count" @click="numplus()">+</button>
            </div>
            </div>
            <div class="area">
                <div class="box1"><button type="button" class="btn btn-num" @click="num0()">0</button>
                </div>
                <div class="box1"><button type="button" class="btn btn-num" @click="num00()">00</button>
                </div>
                <div class="box1"><button type="button" class="btn btn-num" @click="numdot()">.</button>
                </div>
                <div class="box1 box3"><button type="button" class="btn btn-func btn-count" @click="numminus()">-</button>
            </div>
            </div>
            <div class="area">
                <div class="box1"><button type="button" class="btn btn-func" @click="numac()">AC</button>
                </div>
                <div class="box1"><button type="button" class="btn btn-func" @click="numback()">D</button>
                </div>
                <!-- <div class="box2"><button type="button" class="btn btn-num btn-equal" @click="numequal()">=</button> -->
                <div class="box2"><button type="button" class="btn btn-num btn-equal" @click="numequal()">=</button>
            </div>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
    .container{
        width: 300px;
        height: 450px;
        border-radius: 20px;
        background-color: #2f3dd5;
        position: relative;

        .result-area{
            display: flex;
            width: 100%;
            height: 20%;
            border-top-left-radius: 20px;
            border-top-right-radius: 20px;
            background-color: #0b1363;
            position: relative;

            .p1{
                font-size: 20px;
                color: white;
                position: absolute;
                // position: relative;
                // bottom: 10px;
                top: 10px;
                right: 30px;
                // left: 200px;
            }
            // .p1{
            //     width: 100%;
            // }
            p{
                font-size: 60px;
                color: white;
                position: absolute;
                // position: relative;
                // bottom: 10px;
                top: 20px;
                right: 30px;
                // left: 200px;
            }
        }
        .button-area{
            height: 80%;
            position: relative;
            margin: auto;
            justify-content: center;
            align-items: center;
            .area{
                display: flex;

                .box1{
                    display: flex;
                    width: 100px;
                    height: 50px;
                    margin: auto;
                    justify-content: center;
                    align-items: center;
                    border-radius: 10px;
                }

                .box2{
                    display: flex;
                    width: 200px;
                    height: 50px;
                    margin: auto 10px;
                    justify-content: center;
                    align-items: center;
                    background: linear-gradient(to right,  rgb(66, 202, 223), rgb(171, 67, 212));
                    border-radius: 10px;
                }
                .box3{
                    margin: 10px;
                    background-color: #111972;
                    border-radius: 10px;
                }
            }
            .btn{
                font-size: 30px;
                // padding: 3px 24px;
                background-color: #2f3dd5;
                cursor: pointer;
            }
            .btn-num{
                color: white;
            }
            .btn-func{
                color: #9399e0;
            }
            .btn-count{
                background-color: #111972;
            }
            .btn-equal{
                width: 100px;
                // padding: 10px;
                background:none;
            
            }
        }
    }
</style>