import { BrowserRouter as Router, Routes, Route } from "react-router-dom";
import { useEffect } from "react";
import LandingPage from "./components/LandingPage";
import CreateAccount from "./components/CreateAccount";
import LoginPage from "./components/LoginPage";
import ProfileView from "./components/ProfileView";

function App() {
  useEffect(() => {
    document.title = "My React App"; // Sets the tab name
  }, []);

  return (
    <Router>
      <Routes>
        <Route path="/" element={<LandingPage />} />
        <Route path="/create-account" element={<CreateAccount />} />
        <Route path="/login" element={<LoginPage />} />
        <Route path="/profile" element={<ProfileView />} />
      </Routes>
    </Router>
  );
}

export default App;
