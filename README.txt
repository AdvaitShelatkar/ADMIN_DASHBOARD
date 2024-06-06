1) Open terminal using '(Ctrl+Shift+`)' ===> split terminal using '(Ctrl+Shift+5)' 
2) Type 'cd client' in one terminal and 'cd server' in another one 
3) Then type 'npm i' in both terminals 
4) Create a file name '.env' in server folder with following values in it  
	MONGODB_URL = 'your mongodb atlas url' 
	PORT = 1337 
5) Create a file “.env.local” in client folder with following values in it 
	VITE_BASE_URL=http://localhost:1337  
6) Navigate to the 'index.js' file in server folder and uncomment the following lines  
	await mongoose.connection.db.dropDatabase(); 
	KPI.insertMany(kpis); 
	Product.insertMany(products); 
	Transaction.insertMany(transactions); 
7) Type 'npm run dev' in both terminals to run the project