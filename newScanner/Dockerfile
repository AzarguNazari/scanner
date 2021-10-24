FROM arm32v7/node:8
copy . .
# RUN npm install "https://github.com/jrobeson/node-bluetooth-hci-socket/#fix-builds-for-node-10" # worked
RUN apt-get update
RUN apt-get install -y --force-yes --no-install-recommends build-essential libbluetooth-dev libudev-dev

RUN npm install noble --save
RUN npm install node-beacon-scanner --save

CMD ["node", "app.js"]
