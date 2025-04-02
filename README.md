import React from "react"; import { BrowserRouter as Router, Route, Routes, Link } from "react-router-dom"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { Input } from "@/components/ui/input";

const Home = () => (

  <div className="p-4">
    <h1 className="text-2xl font-bold">Welcome to Our Website</h1>
    <nav className="mt-4">
      <Link to="/dashboard" className="mr-4">Dashboard</Link>
      <Link to="/store" className="mr-4">Store</Link>
      <Link to="/news">News</Link>
    </nav>
  </div>
);const Dashboard = () => (

  <div className="p-4">
    <h1 className="text-xl font-bold">Dashboard</h1>
    <Button className="mt-2">Sign In</Button>
    <Button className="mt-2 ml-2">Sign Up</Button>
  </div>
);const Store = () => (

  <div className="p-4">
    <h1 className="text-xl font-bold">Store</h1>
    <div className="grid grid-cols-3 gap-4 mt-4">
      {[1, 2, 3, 4, 5].map((item) => (
        <Card key={item} className="p-2">
          <CardContent>
            <h2 className="text-lg font-semibold">Digital Item {item}</h2>
            <p>Price: ${(item * 10).toFixed(2)}</p>
            <Button className="mt-2">Buy Now</Button>
          </CardContent>
        </Card>
      ))}
    </div>
  </div>
);const News = () => (

  <div className="p-4">
    <h1 className="text-xl font-bold">Latest News</h1>
    <p>Stay updated with the latest news and trends.</p>
  </div>
);const App = () => ( <Router> <Routes> <Route path="/" element={<Home />} /> <Route path="/dashboard" element={<Dashboard />} /> <Route path="/store" element={<Store />} /> <Route path="/news" element={<News />} /> </Routes> </Router> );

export default App;

