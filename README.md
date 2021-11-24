# congenial-lamp
Nigeria History Questions

# TESTT
# !wget https://raw.githubusercontent.com/abhishekq61/tunnel-client/master/linux/staqlab-tunnel.zip

# !unzip ./staqlab-tunnel.zip

import subprocess
import nest_asyncio
import uvicorn
import os

# subprocess.run(["./staqlab-tunnel", "port=10000", "hostname=fish1234"], stdout=subprocess.PIPE)

# !sudo lsof -i -P -n | grep LISTEN

# !sudo lsof -t -i tcp:5000 | xargs kill -9

# nest_asyncio.apply()

# uvicorn.run(app, host="127.0.0.1", port=3000, workers=1)

!nohup lt --port 3000 --subdomain quiztory-1234 & tail -f nohup.out

# !uvicorn main:app --reload

# uvicorn.run(app, host="127.0.0.1", port=5000, workers=1)

# !./staqlab-tunnel port=10000

def start_server():
  nest_asyncio.apply()
  
  uvicorn.run(app, host="127.0.0.1", port=5000, workers=1)

# start_server()



---- 2 -----

code = """
module.paths.push("/tools/node/lib/node_modules");
const localtunnel = require('localtunnel');

(async () => {
  const tunnel = await localtunnel({ port: 5000 });

  // the assigned public url for your tunnel
  // i.e. https://abcdefgjhij.localtunnel.me
  tunnel.url;
  console.log('Public URL at => ', tunnel.url);

  tunnel.on('close', () => {
    // tunnels are closed
    console.log('Closeeeed tunnel');
  });
})();
"""

with open("tunnel.js", "w") as js:
  js.write(code)


!nohup node ./tunnel.js & tail -f nohup.out

nest_asyncio.apply()

uvicorn.run(app, host="127.0.0.1", port=5000, workers=1)

# !npm -g ls --depth=0 --parseable
