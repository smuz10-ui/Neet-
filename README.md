// PyqWebsite.jsx import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Download, ExternalLink } from "lucide-react";

const pyqData = [ { year: 2025, pdfUrl: "path/to/2025.pdf", }, { year: 2024, pdfUrl: "path/to/2024.pdf", }, // Add remaining years till 2015 similarly ];

export default function PyqWebsite() { return ( <div className="min-h-screen bg-gradient-to-br from-white to-[#e0f7f4] p-8"> <h1 className="text-4xl font-bold mb-6 text-center">NEET PYQs (2015 - 2025)</h1> <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6"> {pyqData.map(({ year, pdfUrl }) => ( <Card key={year} className="rounded-2xl shadow-xl"> <CardContent className="p-6 text-center"> <h2 className="text-xl font-semibold mb-4">{year}</h2> <div className="flex justify-center gap-4"> <a href={pdfUrl} download> <Button variant="default" className="flex gap-2"> <Download className="w-4 h-4" /> Download </Button> </a> <a href={pdfUrl} target="_blank" rel="noopener noreferrer"> <Button variant="outline" className="flex gap-2"> <ExternalLink className="w-4 h-4" /> Visit </Button> </a> </div> </CardContent> </Card> ))} </div> </div> ); }


