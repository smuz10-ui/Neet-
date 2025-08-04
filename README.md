// src/PyqWebsite.jsx import React from "react"; import { Download, ExternalLink } from "lucide-react";

const pyqData = [ { year: 2025, pdfUrl: "/pdfs/2025.pdf" }, { year: 2024, pdfUrl: "/pdfs/2024.pdf" }, { year: 2023, pdfUrl: "/pdfs/2023.pdf" }, { year: 2022, pdfUrl: "/pdfs/2022.pdf" }, { year: 2021, pdfUrl: "/pdfs/2021.pdf" }, { year: 2020, pdfUrl: "/pdfs/2020.pdf" }, { year: 2019, pdfUrl: "/pdfs/2019.pdf" }, { year: 2018, pdfUrl: "/pdfs/2018.pdf" }, { year: 2017, pdfUrl: "/pdfs/2017.pdf" }, { year: 2016, pdfUrl: "/pdfs/2016.pdf" }, { year: 2015, pdfUrl: "/pdfs/2015.pdf" }, ];

export default function PyqWebsite() { return ( <div className="min-h-screen bg-gradient-to-br from-white to-[#e0f7f4] p-8"> <h1 className="text-4xl font-bold mb-6 text-center">NEET PYQs (2015 - 2025)</h1> <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6"> {pyqData.map(({ year, pdfUrl }) => ( <div key={year} className="rounded-2xl shadow-xl bg-white p-6 text-center"> <h2 className="text-xl font-semibold mb-4">{year}</h2> <div className="flex justify-center gap-4"> <a href={pdfUrl} download> <button className="bg-blue-500 text-white px-4 py-2 rounded-xl flex gap-2 items-center"> <Download className="w-4 h-4" /> Download </button> </a> <a href={pdfUrl} target="_blank" rel="noopener noreferrer"> <button className="border border-blue-500 text-blue-500 px-4 py-2 rounded-xl flex gap-2 items-center"> <ExternalLink className="w-4 h-4" /> Visit </button> </a> </div> </div> ))} </div> </div> ); }

// ✅ Use this component in src/main.jsx with ReactDOM.render or Vite setup

