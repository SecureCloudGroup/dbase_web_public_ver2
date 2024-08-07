1- Initialize WebRTC:

2- Fetch TURN credentials: [client.js - fetchTurnCredentials]
3- Create a new RTCPeerConnection: [client.js - setupWebRTC]
4- Create a data channel for sending messages: [client.js - setupWebRTC]
5- Set up event handlers for the data channel and ICE candidates: [client.js - setupWebRTC]


6- Set Up WebSocket:

7- Establish a WebSocket connection for signaling: [client.js - initializeWebSocket]
8- Handle incoming WebSocket messages (offers, answers, ICE candidates): [client.js - initializeWebSocket]

9- Create Offer:

10- Create an SDP offer and set it as the local description: [client.js - setupWebRTC]
11- Send the offer to the remote peer via WebSocket: [client.js - setupWebRTC]


12- Handle Offer:

13- When an offer is received, create a new RTCPeerConnection: [client.js - handleOffer]
14- Set the remote description: [client.js - handleOffer]
15- Create an SDP answer and set it as the local description: [client.js - handleOffer]
16- Send the answer back to the remote peer via WebSocket: [client.js - handleOffer]

17- Handle Answer:

18- When an answer is received, set it as the remote description: [client.js - handleAnswer]
19- Handle ICE Candidates:

20- When an ICE candidate is received, add it to the corresponding RTCPeerConnection: [client.js - handleCandidate]


21- Send Message:

22- Ensure the data channel is open: [client.js - sendMessage]
23- Send the message through the data channel: [client.js - sendMessage]
