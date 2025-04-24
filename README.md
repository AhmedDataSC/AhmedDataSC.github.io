import { useState, useEffect } from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Mail, Github, Linkedin } from "lucide-react";

export default function Portfolio() {
  const [form, setForm] = useState({ name: "", email: "", message: "" });
  const [repos, setRepos] = useState([]);

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    alert("Message sent! (This is a placeholder.)");
  };

  useEffect(() => {
    fetch("https://api.github.com/users/AhmedDataSC/repos")
      .then(res => res.json())
      .then(data => setRepos(data.slice(0, 4))) // Get top 4 repos
      .catch(err => console.error(err));
  }, []);

  return (
    <div className="max-w-4xl mx-auto p-6 space-y-12">
      {/* Hero Section */}
      <section className="text-center space-y-4">
        <img src="https://avatars.githubusercontent.com/u/138542786?v=4" alt="Ahmed Raza Ansari" className="w-32 h-32 mx-auto rounded-full shadow-md" />
        <h1 className="text-4xl font-bold">Hi, I'm Ahmed Raza Ansari</h1>
        <p className="text-xl text-gray-600">Data Scientist | ML Enthusiast | Problem Solver</p>
        <div className="flex justify-center space-x-4">
          <a href="mailto:raza123info@gmail.com"><Mail /></a>
          <a href="https://github.com/AhmedDataSC" target="_blank"><Github /></a>
          <a href="https://www.linkedin.com/in/ahmed-raza-ansari-b442a2221" target="_blank"><Linkedin /></a>
        </div>
      </section>

      {/* About Me */}
      <section>
        <h2 className="text-2xl font-semibold mb-2">About Me</h2>
        <p className="text-gray-700">
          I’m Ahmed Raza Ansari, a passionate data scientist with a BCom from Sindh University of Jamshoro (2021),
          currently pursuing Data Science and Artificial Intelligence at NED University of Karachi. I leverage data
          to uncover insights and solve real-world problems.
        </p>
      </section>

      {/* Projects */}
      <section>
        <h2 className="text-2xl font-semibold mb-4">Projects</h2>
        <div className="grid md:grid-cols-2 gap-4">
          {repos.map(repo => (
            <Card key={repo.id}>
              <CardContent className="p-4">
                <h3 className="font-bold text-lg">{repo.name}</h3>
                <p className="text-sm text-gray-600">{repo.description || "No description provided."}</p>
                <a href={repo.html_url} target="_blank" className="text-blue-600 text-sm">View on GitHub</a>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Skills */}
      <section>
        <h2 className="text-2xl font-semibold mb-2">Skills</h2>
        <p className="text-gray-700">
          Python, SQL, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, TensorFlow, Power BI, Tableau
        </p>
      </section>

      {/* Resume */}
      <section className="text-center">
        <Button asChild>
          <a href="/resume.pdf" download>
            Download Resume
          </a>
        </Button>
      </section>

      {/* Contact */}
      <section>
        <h2 className="text-2xl font-semibold mb-4">Contact Me</h2>
        <form onSubmit={handleSubmit} className="space-y-4">
          <Input name="name" placeholder="Your Name" value={form.name} onChange={handleChange} required />
          <Input name="email" placeholder="Your Email" value={form.email} onChange={handleChange} required />
          <Textarea name="message" placeholder="Your Message" value={form.message} onChange={handleChange} required />
          <Button type="submit">Send Message</Button>
        </form>
      </section>
    </div>
  );
}
