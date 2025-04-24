import { useState, useEffect } from "react";
import { Mail, Github, Linkedin, FileText, ArrowRight, Download } from "lucide-react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { motion } from "framer-motion";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";

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
    <div className="max-w-7xl mx-auto px-6 py-10 space-y-24">
      {/* Header */}
      <motion.header
        className="text-center space-y-6"
        initial={{ opacity: 0, y: -50 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
      >
        <img src="https://avatars.githubusercontent.com/u/138542786?v=4" alt="Ahmed Raza Ansari" className="w-32 h-32 mx-auto rounded-full shadow-xl ring-4 ring-blue-500" />
        <h1 className="text-5xl font-extrabold text-gray-800">Ahmed Raza Ansari</h1>
        <p className="text-xl text-gray-600">Data Scientist | ML & AI Explorer | Full-stack Learner</p>
        <div className="flex justify-center space-x-6 text-blue-600">
          <a href="mailto:raza123info@gmail.com" title="Email"><Mail /></a>
          <a href="https://github.com/AhmedDataSC" title="GitHub" target="_blank"><Github /></a>
          <a href="https://www.linkedin.com/in/ahmed-raza-ansari-b442a2221" title="LinkedIn" target="_blank"><Linkedin /></a>
        </div>
      </motion.header>

      {/* Tabs Section */}
      <Tabs defaultValue="about" className="space-y-12">
        <TabsList className="flex justify-center space-x-6 bg-gray-100 p-2 rounded-xl">
          <TabsTrigger value="about">About</TabsTrigger>
          <TabsTrigger value="projects">Projects</TabsTrigger>
          <TabsTrigger value="skills">Skills</TabsTrigger>
          <TabsTrigger value="resume">Resume</TabsTrigger>
          <TabsTrigger value="contact">Contact</TabsTrigger>
        </TabsList>

        <TabsContent value="about">
          <section className="text-center max-w-2xl mx-auto">
            <h2 className="text-3xl font-bold mb-4">About Me</h2>
            <p className="text-lg text-gray-700">
              I'm a passionate data scientist with a BCom from Sindh University of Jamshoro (2021), currently pursuing Data Science and Artificial Intelligence at NED University of Karachi.
              I enjoy solving real-world problems using data and AI. I'm driven by curiosity and love working on projects that blend creativity with technology.
            </p>
          </section>
        </TabsContent>

        <TabsContent value="projects">
          <section>
            <h2 className="text-3xl font-bold mb-6 text-center">Featured Projects</h2>
            <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
              {repos.map(repo => (
                <Card key={repo.id} className="hover:shadow-2xl transition-shadow">
                  <CardContent className="p-4 space-y-2">
                    <h3 className="text-xl font-semibold text-blue-700">{repo.name}</h3>
                    <p className="text-sm text-gray-600">{repo.description || "No description provided."}</p>
                    <div className="flex justify-between text-xs">
                      <span>⭐ {repo.stargazers_count}</span>
                      <a href={repo.html_url} target="_blank" className="text-blue-600 hover:underline flex items-center">View <ArrowRight size={14} className="ml-1" /></a>
                    </div>
                  </CardContent>
                </Card>
              ))}
            </div>
          </section>
        </TabsContent>

        <TabsContent value="skills">
          <section className="text-center">
            <h2 className="text-3xl font-bold mb-4">Skills & Tools</h2>
            <div className="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4 text-gray-700 text-sm">
              <div className="p-3 bg-gray-100 rounded-xl">Python</div>
              <div className="p-3 bg-gray-100 rounded-xl">SQL</div>
              <div className="p-3 bg-gray-100 rounded-xl">Pandas</div>
              <div className="p-3 bg-gray-100 rounded-xl">NumPy</div>
              <div className="p-3 bg-gray-100 rounded-xl">Scikit-learn</div>
              <div className="p-3 bg-gray-100 rounded-xl">Matplotlib</div>
              <div className="p-3 bg-gray-100 rounded-xl">Seaborn</div>
              <div className="p-3 bg-gray-100 rounded-xl">TensorFlow</div>
              <div className="p-3 bg-gray-100 rounded-xl">Power BI</div>
              <div className="p-3 bg-gray-100 rounded-xl">Tableau</div>
            </div>
          </section>
        </TabsContent>

        <TabsContent value="resume">
          <section className="text-center space-y-4">
            <h2 className="text-3xl font-bold">My Resume</h2>
            <Button variant="outline" size="lg" asChild>
              <a href="/resume.pdf" download><Download className="mr-2" />Download Resume</a>
            </Button>
          </section>
        </TabsContent>

        <TabsContent value="contact">
          <section className="max-w-xl mx-auto">
            <h2 className="text-3xl font-bold text-center mb-4">Let's Connect</h2>
            <form onSubmit={handleSubmit} className="space-y-4">
              <Input name="name" placeholder="Your Name" value={form.name} onChange={handleChange} required />
              <Input name="email" type="email" placeholder="Your Email" value={form.email} onChange={handleChange} required />
              <Textarea name="message" placeholder="Your Message" value={form.message} onChange={handleChange} required rows={5} />
              <Button type="submit" className="w-full">Send Message</Button>
            </form>
          </section>
        </TabsContent>
      </Tabs>
    </div>
  );
}
