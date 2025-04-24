import { useState, useEffect } from "react";
import { Mail, Github, Linkedin, FileText } from "lucide-react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { motion } from "framer-motion";

export default function Portfolio() {
  const [form, setForm] = useState({ name: "", email: "", message: "" });
  const [repos, setRepos] = useState([]);

  useEffect(() => {
    fetch("https://api.github.com/users/AhmedDataSC/repos")
      .then(res => res.json())
      .then(data => setRepos(data))
      .catch(err => console.error(err));
  }, []);

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    alert("Message sent! This is a placeholder functionality.");
  };

  return (
    <div className="max-w-6xl mx-auto p-6 space-y-16">
      {/* Header / Hero */}
      <motion.section
        className="text-center space-y-6"
        initial={{ opacity: 0, y: -50 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
      >
        <img src="https://avatars.githubusercontent.com/u/138542786?v=4" alt="Ahmed Raza Ansari" className="w-36 h-36 mx-auto rounded-full border-4 border-blue-500 shadow-lg" />
        <h1 className="text-4xl font-extrabold text-gray-800">Ahmed Raza Ansari</h1>
        <p className="text-lg text-gray-600">Data Scientist | AI Explorer | Full-stack Learner</p>
        <div className="flex justify-center space-x-6">
          <a href="mailto:raza123info@gmail.com" title="Email"><Mail size={24} /></a>
          <a href="https://github.com/AhmedDataSC" title="GitHub" target="_blank"><Github size={24} /></a>
          <a href="https://www.linkedin.com/in/ahmed-raza-ansari-b442a2221" title="LinkedIn" target="_blank"><Linkedin size={24} /></a>
        </div>
      </motion.section>

      {/* About Section */}
      <section className="space-y-4">
        <h2 className="text-3xl font-bold">About Me</h2>
        <p className="text-gray-700 text-lg">
          I'm a passionate data scientist with a BCom from Sindh University of Jamshoro (2021), currently pursuing a degree in Data Science and Artificial Intelligence at NED University of Karachi. I thrive on extracting insights from complex data and building solutions using AI and machine learning.
        </p>
      </section>

      {/* Projects Section */}
      <section className="space-y-6">
        <h2 className="text-3xl font-bold">Projects</h2>
        <div className="grid gap-6 md:grid-cols-2">
          {repos.map((repo) => (
            <Card key={repo.id} className="hover:shadow-xl transition-shadow duration-300">
              <CardContent className="p-5">
                <h3 className="text-xl font-semibold text-blue-700">{repo.name}</h3>
                <p className="text-gray-600 text-sm mb-2">{repo.description || "No description provided."}</p>
                <div className="flex justify-between text-sm">
                  <span>⭐ {repo.stargazers_count}</span>
                  <a href={repo.html_url} target="_blank" className="text-blue-600 hover:underline">View on GitHub</a>
                </div>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Skills Section */}
      <section className="space-y-4">
        <h2 className="text-3xl font-bold">Skills</h2>
        <ul className="grid grid-cols-2 md:grid-cols-3 gap-2 text-gray-700">
          <li>Python</li>
          <li>SQL</li>
          <li>Pandas</li>
          <li>NumPy</li>
          <li>Scikit-learn</li>
          <li>Matplotlib</li>
          <li>Seaborn</li>
          <li>TensorFlow</li>
          <li>Power BI</li>
          <li>Tableau</li>
        </ul>
      </section>

      {/* Resume Section */}
      <section className="text-center">
        <Button asChild className="text-lg">
          <a href="/resume.pdf" download>
            <FileText className="inline-block mr-2" /> Download My Resume
          </a>
        </Button>
      </section>

      {/* Contact Form */}
      <section className="space-y-6">
        <h2 className="text-3xl font-bold">Contact Me</h2>
        <form onSubmit={handleSubmit} className="space-y-4 max-w-xl mx-auto">
          <Input name="name" placeholder="Your Name" value={form.name} onChange={handleChange} required />
          <Input name="email" placeholder="Your Email" value={form.email} onChange={handleChange} required />
          <Textarea name="message" placeholder="Your Message" value={form.message} onChange={handleChange} required rows={5} />
          <Button type="submit" className="w-full">Send Message</Button>
        </form>
      </section>
    </div>
  );
}
