# Best
import React, { useState, useEffect } from 'react';
import { 
  Calculator, 
  DollarSign, 
  TrendingUp, 
  Percent, 
  Truck, 
  Info,
  Lock,
  Key,
  Eye,
  EyeOff,
  Copy,
  Check,
  Settings2,
  RefreshCw
} from 'lucide-react';

/**
 * PriceArchitect Pro - PWA Version
 * This file contains the complete logic for pricing, encoding, and UI.
 * Designed for standalone mobile use.
 */

const App = () => {
  const [costPrice, setCostPrice] = useState(100);
  const [overhead, setOverhead] = useState(5);
  const [markupOrMargin, setMarkupOrMargin] = useState(30);
  const [taxRate, setTaxRate] = useState(10);
  const [mode, setMode] = useState('markup'); 
  const [secretKey, setSecretKey] = useState('BLACKHORSE'); 
  const [showKey, setShowKey] = useState(false);
  const [copied, setCopied] = useState(false);

  const [results, setResults] = useState({
    sellingPrice: 0,
    profit: 0,
    actualMargin: 0,
    taxAmount: 0,
    totalCost: 0,
    encodedPrice: '',
    encodedCost: ''
  });

  const encodeValue = (val, key) => {
    if (!key || key.length < 10) return "INVALID KEY";
    const cleanValue = val.toFixed(2).toString();
    let encoded = "";
    for (let char of cleanValue) {
      if (char === '.') {
        encoded += '.'; 
      } else if (!isNaN(parseInt(char))) {
        encoded += key[parseInt(char)].toUpperCase();
      }
    }
    return encoded;
  };

  useEffect(() => {
    const cp = parseFloat(costPrice) || 0;
    const oh = parseFloat(overhead) || 0;
    const totalCost = cp + oh;
    const target = parseFloat(markupOrMargin) || 0;
    const tax = parseFloat(taxRate) || 0;

    let subtotal = 0;
    if (mode === 'markup') {
      subtotal = totalCost * (1 + target / 100);
    } else {
      const marginDecimal = target / 100;
      subtotal = marginDecimal >= 1 ? totalCost * 10 : totalCost / (1 - marginDecimal);
    }

    const taxAmount = subtotal * (tax / 100);
    const finalPrice = subtotal + taxAmount;
    const profit = subtotal - totalCost;
    const actualMargin = subtotal > 0 ? (profit / subtotal) * 100 : 0;

    setResults({
      sellingPrice: finalPrice,
      profit: profit,
      actualMargin: actualMargin,
      taxAmount: taxAmount,
      totalCost: totalCost,
      encodedPrice: encodeValue(finalPrice, secretKey),
      encodedCost: encodeValue(totalCost, secretKey)
    });
  }, [costPrice, overhead, markupOrMargin, taxRate, mode, secretKey]);

  const copyToClipboard = (text) => {
    const el = document.createElement('textarea');
    el.value = text;
    document.body.appendChild(el);
    el.select();
    document.execCommand('copy');
    document.body.removeChild(el);
    setCopied(true);
    setTimeout(() => setCopied(false), 2000);
  };

  const formatCurrency = (value) => {
    return new Intl.NumberFormat('en-US', {
      style: 'currency',
      currency: 'USD',
    }).format(value);
  };

  return (
    <div className="min-h-screen bg-slate-50 font-sans text-slate-900 pb-20 select-none">
      {/* Header with App-like feel */}
      <header className="bg-white border-b border-slate-200 sticky top-0 z-30 px-4 py-4 shadow-sm safe-top">
        <div className="max-w-xl mx-auto flex items-center justify-between">
          <div className="flex items-center gap-2">
            <div className="p-1.5 bg-indigo-600 text-white rounded-lg">
              <Calculator size={20} />
            </div>
            <h1 className="text-lg font-black tracking-tight">PriceArchitect</h1>
          </div>
          
          <div className="flex items-center gap-2 bg-slate-100 p-1 rounded-full border border-slate-200">
            <Key size={12} className="ml-2 text-amber-500" />
            <input
              type={showKey ? "text" : "password"}
              maxLength={10}
              value={secretKey}
              onChange={(e) => setSecretKey(e.target.value.toUpperCase().replace(/[^A-Z]/g, ''))}
              className="bg-transparent border-none text-[10px] font-mono font-bold tracking-widest focus:ring-0 w-20 p-0"
            />
            <button onClick={() => setShowKey(!showKey)} className="p-1 hover:bg-white rounded-full transition-colors">
              {showKey ? <EyeOff size={12} /> : <Eye size={12} />}
            </button>
          </div>
        </div>
      </header>

      <main className="max-w-xl mx-auto px-4 mt-4 space-y-4">
        {/* Results Card - Large for Mobile Visibility */}
        <div className="bg-white rounded-[2rem] border-2 border-indigo-100 shadow-xl shadow-indigo-50/50 overflow-hidden">
          <div className="p-6 text-center">
            <p className="text-[10px] font-bold text-slate-400 uppercase tracking-widest mb-1">Selling Price</p>
            <h3 className="text-5xl font-black text-slate-900 tracking-tighter mb-4">
              {formatCurrency(results.sellingPrice)}
            </h3>
            
            <div className="bg-indigo-600 rounded-2xl p-4 text-white relative group active:scale-95 transition-transform shadow-lg shadow-indigo-200">
              <div className="flex flex-col items-center gap-1">
                <span className="text-[9px] font-black text-indigo-200 uppercase tracking-widest">Secret Tag Code</span>
                <div className="flex items-center gap-3">
                  <span className="text-3xl font-mono font-black tracking-[0.2em]">
                    {results.encodedPrice}
                  </span>
                  <button onClick={() => copyToClipboard(results.encodedPrice)} className="p-2 bg-white/10 rounded-lg">
                    {copied ? <Check size={16} /> : <Copy size={16} />}
                  </button>
                </div>
              </div>
            </div>
          </div>

          <div className="grid grid-cols-2 border-t border-slate-50 bg-slate-50/50">
            <div className="p-4 text-center border-r border-slate-50">
              <p className="text-[9px] font-bold text-slate-400 uppercase">Net Profit</p>
              <p className="text-lg font-black text-green-600">{formatCurrency(results.profit)}</p>
            </div>
            <div className="p-4 text-center">
              <p className="text-[9px] font-bold text-slate-400 uppercase">Margin</p>
              <p className="text-lg font-black text-slate-800">{results.actualMargin.toFixed(1)}%</p>
            </div>
          </div>
        </div>

        {/* Inputs */}
        <div className="bg-white rounded-3xl p-5 shadow-sm border border-slate-200 space-y-4">
          <div className="grid grid-cols-2 gap-4">
            <div>
              <label className="block text-[10px] font-black text-slate-400 uppercase mb-1 ml-1">Cost Price</label>
              <div className="relative">
                <input
                  type="number"
                  value={costPrice}
                  onChange={(e) => setCostPrice(e.target.value)}
                  className="w-full pl-4 pr-4 py-3 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-indigo-500 outline-none font-bold"
                />
              </div>
            </div>
            <div>
              <label className="block text-[10px] font-black text-slate-400 uppercase mb-1 ml-1">Overhead</label>
              <input
                type="number"
                value={overhead}
                onChange={(e) => setOverhead(e.target.value)}
                className="w-full px-4 py-3 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-indigo-500 outline-none font-bold"
              />
            </div>
          </div>

          <div>
            <div className="flex bg-slate-100 p-1 rounded-xl mb-4">
              {['markup', 'margin'].map((m) => (
                <button
                  key={m}
                  onClick={() => setMode(m)}
                  className={`flex-1 py-2 text-[10px] font-black uppercase rounded-lg transition-all ${
                    mode === m ? 'bg-white text-indigo-600 shadow-sm' : 'text-slate-500'
                  }`}
                >
                  {m}
                </button>
              ))}
            </div>
            <div className="flex justify-between items-center mb-1 px-1">
              <span className="text-[10px] font-black text-slate-400 uppercase">Target {mode}</span>
              <span className="text-xs font-bold text-indigo-600">{markupOrMargin}%</span>
            </div>
            <input
              type="range"
              min="0"
              max={mode === 'margin' ? "90" : "200"}
              value={markupOrMargin}
              onChange={(e) => setMarkupOrMargin(e.target.value)}
              className="w-full h-1.5 bg-slate-200 rounded-lg appearance-none cursor-pointer accent-indigo-600"
            />
          </div>
        </div>

        {/* Cost Reference */}
        <div className="bg-slate-900 rounded-2xl p-4 text-white flex justify-between items-center">
          <div className="flex items-center gap-2">
            <Info size={14} className="text-indigo-400" />
            <span className="text-[10px] font-bold uppercase tracking-widest">Internal Cost Code</span>
          </div>
          <span className="font-mono font-bold text-indigo-400 tracking-widest">{results.encodedCost}</span>
        </div>
      </main>

      {/* Persistent Bottom Label for PWA */}
      <footer className="fixed bottom-4 left-4 right-4 text-center">
         <p className="text-[8px] text-slate-300 font-bold uppercase tracking-widest">
           PriceArchitect v1.0 • Enterprise Edition
         </p>
      </footer>
    </div>
  );
};

export default App;

