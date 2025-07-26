// RaoClip.ai - AI-Powered YouTube Clip Editor

import React, { useState } from "react"; import { Input } from "@/components/ui/input"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs"; import { Switch } from "@/components/ui/switch"; import { Sun, Moon } from "lucide-react"; import { motion } from "framer-motion";

export default function RaoClip() { const [url, setUrl] = useState(""); const [darkMode, setDarkMode] = useState(false); const [clipReady, setClipReady] = useState(false); const [caption, setCaption] = useState("");

const handleProcess = () => { // Simulated clip process setTimeout(() => { setClipReady(true); setCaption("This is an auto-generated caption ✨"); }, 2000); };

return ( <div className={darkMode ? "bg-black text-white min-h-screen" : "bg-white text-black min-h-screen"}> <div className="flex justify-between items-center px-6 py-4 shadow-md"> <h1 className="text-2xl font-bold">RaoClip.ai 🎬</h1> <div className="flex items-center space-x-2"> <Sun /> <Switch checked={darkMode} onCheckedChange={setDarkMode} /> <Moon /> </div> </div>

<motion.div
    initial={{ opacity: 0, y: 20 }}
    animate={{ opacity: 1, y: 0 }}
    transition={{ duration: 0.5 }}
    className="max-w-xl mx-auto p-6"
  >
    <Card>
      <CardContent className="space-y-4 py-6">
        <Input
          placeholder="Paste YouTube video URL here..."
          value={url}
          onChange={(e) => setUrl(e.target.value)}
        />
        <Button onClick={handleProcess} disabled={!url}>Process Clip</Button>
      </CardContent>
    </Card>

    {clipReady && (
      <motion.div
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ duration: 0.5 }}
        className="mt-6 space-y-4"
      >
        <h2 className="text-xl font-semibold">🎞️ Clip Preview</h2>
        <div className="w-full h-48 bg-gray-300 rounded-xl flex items-center justify-center">
          <span className="text-gray-700">[Video Clip Preview Here]</span>
        </div>
        <h3 className="font-medium">📝 Auto Caption</h3>
        <p className="bg-gray-100 dark:bg-gray-800 p-4 rounded-xl">{caption}</p>
      </motion.div>
    )}
  </motion.div>
</div>

); }

// RaoClip.ai - AI-Powered YouTube Clip Editor

import React, { useState } from "react"; import { Input } from "@/components/ui/input"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs"; import { Switch } from "@/components/ui/switch"; import { Sun, Moon } from "lucide-react"; import { motion } from "framer-motion";

export default function RaoClip() { const [url, setUrl] = useState(""); const [darkMode, setDarkMode] = useState(false); const [clipReady, setClipReady] = useState(false); const [caption, setCaption] = useState("");

const handleProcess = () => { // Simulated clip process setTimeout(() => { setClipReady(true); setCaption("This is an auto-generated caption ✨"); }, 2000); };

return ( <div className={darkMode ? "bg-black text-white min-h-screen" : "bg-white text-black min-h-screen"}> <div className="flex justify-between items-center px-6 py-4 shadow-md"> <h1 className="text-2xl font-bold">RaoClip.ai 🎬</h1> <div className="flex items-center space-x-2"> <Sun /> <Switch checked={darkMode} onCheckedChange={setDarkMode} /> <Moon /> </div> </div>

<motion.div
    initial={{ opacity: 0, y: 20 }}
    animate={{ opacity: 1, y: 0 }}
    transition={{ duration: 0.5 }}
    className="max-w-xl mx-auto p-6"
  >
    <Card>
      <CardContent className="space-y-4 py-6">
        <Input
          placeholder="Paste YouTube video URL here..."
          value={url}
          onChange={(e) => setUrl(e.target.value)}
        />
        <Button onClick={handleProcess} disabled={!url}>Process Clip</Button>
      </CardContent>
    </Card>

    {clipReady && (
      <motion.div
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ duration: 0.5 }}
        className="mt-6 space-y-4"
      >
        <h2 className="text-xl font-semibold">🎞️ Clip Preview</h2>
        <div className="w-full h-48 bg-gray-300 rounded-xl flex items-center justify-center">
          <span className="text-gray-700">[Video Clip Preview Here]</span>
        </div>
        <h3 className="font-medium">📝 Auto Caption</h3>
        <p className="bg-gray-100 dark:bg-gray-800 p-4 rounded-xl">{caption}</p>
      </motion.div>
    )}
  </motion.div>
</div>

); }

