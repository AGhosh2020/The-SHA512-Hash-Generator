<script>
        import { sha512 } from 'js-sha512';
        let string="";
        let error="";
        let hashString = "";

        function HashTheString(){
            if(string.trim().length<1){
                hashString = "";
            }
            else
            {
                hashString=sha512(string);
                error = "";
            }
        }
        function ClearAll(){
                string="";
                hashString = "";
                error = "";
        }

        function CopyToClipboard(){
            if(hashString.trim().length<1){
                error = "Generate SHA512 hashed string first then click copy";
            }
            else{
                document.getElementById("hashedString").select();
                document.execCommand('copy');

            }
        }
</script>
<work>

    <div class="sha512gen">
        <p>Enter your information below:</p>
            <textarea bind:value={string} on:input={HashTheString} placeholder="Input......"></textarea> 
            <table>
                <tr>
                    <td><button type="reset" on:click={ClearAll}>Clear all</button></td>
                </tr>
            </table>        
    </div>
        <p style="text-align:center;">Generated SHA512 of your string: [<span class="copy" on:click={CopyToClipboard}>Copy to clipboard</span>]</p>

        <div class="generated512">
            <div class="error" style="text-align:center;">{error}</div>
            <textarea id="hashedString" bind:value={hashString} readonly placeholder="Output......"></textarea>
        </div>
    
</work>
<style>
    button{
        background-color: #465773;
        padding:10px;
        margin: 4px 2px;
        border: 1px solid #465773;
        border-radius: 10px;
        text-transform: uppercase;
        cursor:pointer;
        color:white;
    }
    button:hover{
        background-color: #6c7f9e;
        border-radius: 1px solid #6c7f9e;
    }
    button:active{
        background-color: #7b89a1;
        border-radius: 1px solid #7b89a1;
    }
    textarea{ 
        width: 100%; 
        height: 200px; 
        transition: background-color 0.9s;
    }
    table{
        margin-left: auto;
        margin-right: auto;   
    }
  
    .error{
        color:red;
        font-size: bold;
        margin-bottom:1px;
    }
    :global(body.dark) textarea {
        background-color: black;
		color: #FFFFFF;
        transition: background-color 0.9s;
	}
    .copy{
        cursor: pointer;
        color:blue;
    }
    .copy:hover{
        color:blueviolet;
    }
    .copy:active{
        color:rgb(104, 82, 122);
    }
    :global(body.dark) .copy{
        color:rgb(103, 103, 248);
    }
    :global(body.dark) .copy:active{
        color:#FFFFFF;
    }
</style>