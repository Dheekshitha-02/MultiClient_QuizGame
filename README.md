# MultiClient_QuizGame

## 🧩 Quiz Game Over TCP Sockets (C Language)
This is a C-based terminal quiz game built using client-server architecture with TCP sockets. The client connects to the server, receives questions, and sends answers. The server validates them, times the responses, and displays a scoreboard with results and winner(s).

## 🎯 Features
- Developed in pure C using socket programming

- Real-time multiple-choice quiz with a 60-second time limit per question

- Validates answers and tracks response time

- Scoreboard displays individual timings and total time

- Handles multiple client sessions (via fork)

- Tracks winner(s) based on lowest total time

## 🗂️ File Structure

bash
```
quiz_game/
├── gamec.c             # Client code
├── games.c             # Server code
├── times.txt           # Auto-generated log of time per user
├── total.txt           # Auto-generated winner data
├── client_1.png ...    # Screenshots of client executions
```

## 🛠️ How to Compile and Run

### Step 1: Compile the server and client

bash
```
gcc games.c -o server
gcc gamec.c -o client
```
### Step 2: Run the server
bash
```
./server
```
### Step 3: Run the client (in another terminal or machine
bash
```
./client
```

## 📝 Notes
- If the client answers a question incorrectly or takes more than 60 seconds, the session ends.

- All scores and timings are saved in times.txt and total.txt files.

- Multiple clients can compete, and the lowest total response time wins.
