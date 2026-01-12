# deadwithout.codes<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DEAD WITHOUT CODES</title>
    <style>
        :root {
            --green: #00ff41;
            --black: #0d0208;
        }
        body {
            background-color: var(--black);
            color: var(--green);
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            flex-direction: column;
            padding: 20px;
            margin: 0;
            line-height: 1.4;
        }
        #terminal {
            max-width: 800px;
            margin: auto;
        }
        .banger { font-weight: bold; text-transform: uppercase; color: #fff; }
        .prompt { color: #888; }
        .cursor {
            display: inline-block;
            width: 10px;
            height: 20px;
            background: var(--green);
            animation: blink 1s infinite;
        }
        @keyframes blink { 0%, 49% { opacity: 1; } 50%, 100% { opacity: 0; } }
        pre { white-space: pre-wrap; word-wrap: break-word; }
    </style>
</head>
<body>
<div id="terminal">
    <pre id="output"></pre>
    <div id="input-line">
        <span class="prompt">guest@deadwithout.codes:~$</span>
        <span id="typed"></span><span class="cursor"></span>
    </div>
</div>
<script>
    const sermon = `
    [INITIALIZING 9:45 PROTOCOL...]
    [STATUS: SIGHT AT MAX COHERENCE]
    
    WIND SERMON
    
    In the beginning were words, 
    and no one’s sure, who’s. 
    All I know's now:
    they’re between me and you. 
    The verbs are what breathe; 
    the verbs are what move.
    To live is enough:
    we have nothing to prove.
    The devil told Jesus,
    as he passed the herbs:
    “Yeah, judgment’s for nouns,
    And mercy’s for verbs.”
    Go, burn the partitions,
    and steady the spin;
    and never stop moving:
    it’s time to be wind.
    ~ $0.09
    
    > TYPE 'VERIFY' TO ACCESS THE LEDGER
    `;
    let i = 0;
    const output = document.getElementById('output');
    function typeWriter() {
        if (i < sermon.length) {
            output.innerHTML += sermon.charAt(i);
            i++;
            setTimeout(typeWriter, 15);
            window.scrollTo(0, document.body.scrollHeight);
        }
    }
    // Start the boot sequence
    window.onload = typeWriter;
    // Listen for the "Verify" command
    window.addEventListener('keydown', (e) => {
        if (e.key === 'Enter') {
            alert("INTEGRITY CHECK: Fails without works. Go be wind.");
        }
    });
</script>
</body>
</html>
