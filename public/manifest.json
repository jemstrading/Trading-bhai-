import { useState, useEffect } from 'react';
import {
  ChevronLeft,
  Award,
  TrendingUp,
  BarChart2,
  DollarSign,
  Briefcase,
  Layers,
  HeartHandshake,
  Brain,
  Sparkles
} from 'lucide-react';

// Define the data for the structured learning content in Hindi
const categories = [
  {
    id: 'intro-to-markets',
    title: 'बाजारों का परिचय',
    icon: <Briefcase size={48} />,
    lessons: [
      {
        id: 'trading-vs-investing',
        title: 'ट्रेडिंग बनाम इन्वेस्टिंग',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">ट्रेडिंग बनाम इन्वेस्टिंग</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              यह वित्तीय बाजारों में दो अलग-अलग दृष्टिकोण हैं।
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li><strong>इन्वेस्टिंग (निवेश):</strong> इसका लक्ष्य लंबी अवधि में पूंजी बढ़ाना है। इन्वेस्टर्स आमतौर पर वर्षों या दशकों तक शेयर रखते हैं और कंपनी के मौलिक मूल्य (fundamental value) पर ध्यान केंद्रित करते हैं।</li>
              <li><strong>ट्रेडिंग:</strong> इसका लक्ष्य छोटी अवधि में, कीमतों के उतार-चढ़ाव से लाभ कमाना है। ट्रेडर्स कुछ मिनटों से लेकर कुछ महीनों तक शेयर रखते हैं और तकनीकी विश्लेषण (technical analysis) का उपयोग करते हैं।</li>
            </ul>
            <p className="text-gray-700 leading-relaxed">
              निवेशक अक्सर "Buy and Hold" की रणनीति अपनाते हैं, जबकि ट्रेडर "Buy Low, Sell High" या "Sell High, Buy Low" जैसी रणनीति पर काम करते हैं।
            </p>
          </>
        ),
      },
      {
        id: 'types-of-markets',
        title: 'वित्तीय बाजारों के प्रकार',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">वित्तीय बाजारों के प्रकार</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              निवेश और ट्रेडिंग के लिए कई तरह के वित्तीय बाजार उपलब्ध हैं:
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li><strong>स्टॉक मार्केट:</strong> यहाँ कंपनियों के शेयरों का व्यापार होता है। भारत में NSE और BSE प्रमुख स्टॉक एक्सचेंज हैं।</li>
              <li><strong>कमोडिटी मार्केट:</strong> यहाँ सोना, चांदी, कच्चा तेल और कृषि उत्पादों जैसी कमोडिटीज का व्यापार होता है।</li>
              <li><strong>फॉरेक्स (विदेशी मुद्रा) मार्केट:</strong> यहाँ विभिन्न देशों की मुद्राओं का व्यापार होता है। यह दुनिया का सबसे बड़ा और सबसे अधिक लिक्विड बाजार है।</li>
              <li><strong>डेरिवेटिव्स मार्केट:</strong> इसमें Futures और Options जैसे वित्तीय उपकरण शामिल हैं, जिनका मूल्य एक अंतर्निहित संपत्ति (underlying asset) से लिया जाता है।</li>
            </ul>
          </>
        ),
      },
    ],
  },
  {
    id: 'fundamental-analysis',
    title: 'मौलिक विश्लेषण',
    icon: <DollarSign size={48} />,
    lessons: [
      {
        id: 'what-is-fa',
        title: 'मौलिक विश्लेषण क्या है?',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">मौलिक विश्लेषण क्या है?</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              मौलिक विश्लेषण किसी कंपनी के आंतरिक मूल्य (intrinsic value) का मूल्यांकन करने की एक विधि है। इसका उद्देश्य यह पता लगाना है कि क्या कोई शेयर अपनी वास्तविक कीमत से कम या ज्यादा मूल्य पर ट्रेड हो रहा है।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              इसमें कंपनी के वित्तीय विवरण (financial statements), प्रबंधन, प्रतिस्पर्धी माहौल और उद्योग के रुझानों का गहन अध्ययन शामिल होता है।
            </p>
          </>
        ),
      },
      {
        id: 'key-financial-statements',
        title: 'प्रमुख वित्तीय विवरण',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">प्रमुख वित्तीय विवरण</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              तीन प्रमुख वित्तीय विवरण हैं जिन्हें हर निवेशक को पढ़ना आना चाहिए:
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li><strong>आय विवरण (Income Statement):</strong> यह एक निश्चित अवधि में कंपनी के राजस्व, खर्चों और लाभ (Profit & Loss) को दर्शाता है।</li>
              <li><strong>बैलेंस शीट (Balance Sheet):</strong> यह एक निश्चित समय पर कंपनी की संपत्ति (assets), देनदारियों (liabilities) और शेयरधारक इक्विटी (equity) का स्नैपशॉट है।</li>
              <li><strong>नकद प्रवाह विवरण (Cash Flow Statement):</strong> यह दिखाता है कि कंपनी में और बाहर कितना नकद (cash) आया और गया।</li>
            </ul>
          </>
        ),
      },
      {
        id: 'valuation-metrics',
        title: 'महत्वपूर्ण मूल्यांकन अनुपात',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">महत्वपूर्ण मूल्यांकन अनुपात</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              कंपनियों का मूल्यांकन करने के लिए कुछ प्रमुख अनुपातों का उपयोग किया जाता है:
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li><strong>P/E (Price-to-Earnings) Ratio:</strong> यह दर्शाता है कि निवेशक कंपनी की प्रति शेयर आय (earnings per share) के लिए कितना भुगतान करने को तैयार हैं।</li>
              <li><strong>P/B (Price-to-Book) Ratio:</strong> यह कंपनी के बाजार मूल्य की तुलना उसके बुक वैल्यू से करता है।</li>
              <li><strong>Debt-to-Equity Ratio:</strong> यह दिखाता है कि कंपनी ने अपनी फंडिंग के लिए कितना कर्ज लिया है।</li>
              <li><strong>ROE (Return on Equity):</strong> यह कंपनी की लाभप्रदता (profitability) को मापता है।</li>
            </ul>
          </>
        ),
      },
    ],
  },
  {
    id: 'technical-analysis',
    title: 'तकनीकी विश्लेषण',
    icon: <BarChart2 size={48} />,
    lessons: [
      {
        id: 'what-is-ta',
        title: 'तकनीकी विश्लेषण क्या है?',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">तकनीकी विश्लेषण क्या है?</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              तकनीकी विश्लेषण एक विधि है जिसमें भविष्य की कीमतों की भविष्यवाणी करने के लिए पिछले कीमतों और ट्रेडिंग वॉल्यूम का अध्ययन किया जाता है। यह इस धारणा पर आधारित है कि इतिहास खुद को दोहराता है और सभी जानकारी पहले से ही कीमत में शामिल होती है।
            </p>
            <p className="text-gray-700 leading-relaxed">
              इसमें candlestick charts, trendlines, समर्थन और प्रतिरोध (support and resistance) जैसे उपकरणों का उपयोग किया जाता है।
            </p>
          </>
        ),
      },
      {
        id: 'support-resistance-trendlines',
        title: 'समर्थन, प्रतिरोध और ट्रेंडलाइन',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">समर्थन, प्रतिरोध और ट्रेंडलाइन</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              ये तकनीकी विश्लेषण के सबसे बुनियादी और महत्वपूर्ण अवधारणाएं हैं:
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li><strong>समर्थन (Support):</strong> यह वह मूल्य स्तर है जहाँ खरीददार आने की उम्मीद होती है, जिससे कीमत गिरने से रुकती है।</li>
              <li><strong>प्रतिरोध (Resistance):</strong> यह वह मूल्य स्तर है जहाँ बेचक (sellers) आने की उम्मीद होती है, जिससे कीमत बढ़ने से रुकती है।</li>
              <li><strong>ट्रेंडलाइन (Trendline):</strong> यह एक लाइन है जो चार्ट पर समर्थन या प्रतिरोध को दर्शाने के लिए खींची जाती है। यह बाजार की दिशा (trend) को समझने में मदद करती है।</li>
            </ul>
            <img src="https://placehold.co/600x300/e9ecef/212529?text=Support+और+Resistance" alt="समर्थन और प्रतिरोध का उदाहरण" className="rounded-lg shadow-md mb-4 w-full" />
            <p className="text-sm italic text-gray-500 text-center">
              ऊपर दिए गए चार्ट में, नीली रेखाएँ समर्थन और प्रतिरोध के स्तरों को दिखाती हैं।
            </p>
          </>
        ),
      },
      {
        id: 'candlestick-patterns',
        title: 'कैंडलस्टिक पैटर्न्स',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">कैंडलस्टिक पैटर्न्स</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              कैंडलस्टिक चार्ट, price movement को visual रूप से समझने का एक बहुत ही लोकप्रिय तरीका है। हर कैंडल एक निश्चित समय-सीमा के लिए चार महत्वपूर्ण कीमतें दिखाती है: Open, High, Low, और Close।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              कुछ महत्वपूर्ण पैटर्न्स में शामिल हैं:
            </p>
            <img src="https://placehold.co/600x300/27ae60/ecf0f1?text=Bullish+Candlestick+Patterns" alt="कैंडलस्टिक पैटर्न्स का उदाहरण" className="rounded-lg shadow-md mb-4 w-full" />
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li><strong>Doji:</strong> दर्शाता है कि खरीदारों और विक्रेताओं के बीच अनिर्णय की स्थिति है।</li>
              <li><strong>Hammer:</strong> आमतौर पर एक downtrend के अंत में दिखता है और संभावित reversal का संकेत देता है।</li>
              <li><strong>Engulfing Pattern:</strong> यह एक मजबूत reversal signal हो सकता है, जहाँ एक बड़ी कैंडल पिछली छोटी कैंडल को पूरी तरह से घेर लेती है।</li>
            </ul>
          </>
        ),
      },
      {
        id: 'indicators-and-oscillators',
        title: 'संकेतक (Indicators) और ऑसिलेटर',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">संकेतक (Indicators) और ऑसिलेटर</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              संकेतक गणितीय गणनाएँ हैं जो कीमत और मात्रा पर आधारित होती हैं और ट्रेडर को निर्णय लेने में मदद करती हैं।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              इसमें दो बहुत लोकप्रिय indicators हैं:
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li><strong>मूविंग एवरेज (Moving Averages):</strong> यह एक निश्चित अवधि में औसत मूल्य को दर्शाता है और रुझान (trend) को smooth करता है।</li>
              <li><strong>RSI (Relative Strength Index):</strong> यह एक ऑसिलेटर है जो बताता है कि कोई संपत्ति अधिक खरीदी गई है (overbought) या अधिक बेची गई है (oversold)।</li>
              <li><strong>MACD (Moving Average Convergence Divergence):</strong> यह दो मूविंग एवरेज के बीच के संबंध को दर्शाता है और रुझान की ताकत और दिशा को बताता है।</li>
            </ul>
          </>
        ),
      },
      {
        id: 'bollinger-bands',
        title: 'बोलेन्जर बैंड्स (Bollinger Bands)',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">बोलेन्जर बैंड्स</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              बोलेन्जर बैंड्स एक volatility indicator है। इसमें तीन लाइनें होती हैं: एक Simple Moving Average (मध्य रेखा), और दो standard deviation lines (ऊपरी और निचली रेखा)।
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li>जब बैंड्स सिकुड़ते हैं, तो यह कम volatility का संकेत है, जिसके बाद आमतौर पर एक बड़ा price movement होता है।</li>
              <li>जब बैंड्स फैलते हैं, तो यह high volatility का संकेत है।</li>
              <li>कीमतें अक्सर बैंड्स के भीतर रहती हैं; जब वे ऊपरी या निचली रेखा को छूती हैं, तो तो यह reversal का संकेत हो सकता है।</li>
            </ul>
            <img src="https://placehold.co/600x300/4F46E5/FFFFFF?text=Bollinger+Bands+Chart" alt="बोलेन्जर बैंड्स का उदाहरण" className="rounded-lg shadow-md mb-4 w-full" />
          </>
        ),
      },
    ],
  },
  {
    id: 'advanced-analysis',
    title: 'उन्नत विश्लेषण',
    icon: <TrendingUp size={48} />,
    lessons: [
      {
        id: 'fibonacci-retracement',
        title: 'फाइबोनैचि रिट्रेसमेंट',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">फाइबोनैचि रिट्रेसमेंट क्या है?</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              फाइबोनैचि रिट्रेसमेंट एक technical analysis tool है जिसका उपयोग किसी asset के support और resistance levels को निर्धारित करने के लिए किया जाता है। यह इस विचार पर आधारित है कि market, price में एक महत्वपूर्ण movement के बाद, आंशिक रूप से वापस उसी दिशा में आता है।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              इसमें कुछ प्रमुख स्तर ($23.6\%$, $38.2\%$, $50\%$, $61.8\%$, और $78.6\%$) होते हैं जहाँ price के मुड़ने (retrace) की संभावना होती है।
            </p>
            <img src="https://placehold.co/600x300/e9ecef/212529?text=Fibonacci+Retracement+Levels" alt="फाइबोनैचि रिट्रेसमेंट का उदाहरण" className="rounded-lg shadow-md mb-4 w-full" />
            <p className="text-sm italic text-gray-500 text-center">
              ऊपर दिए गए चार्ट में, फाइबोनैचि रिट्रेसमेंट स्तरों को दिखाया गया है।
            </p>
          </>
        ),
      },
      {
        id: 'elliot-wave-theory',
        title: 'इलियट वेव थ्योरी',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">इलियट वेव थ्योरी</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              इलियट वेव थ्योरी यह बताती है कि बाजार की कीमतें predictable patterns में चलती हैं, जो कि traders की psychology को दर्शाती हैं।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              इस थ्योरी के अनुसार, market trend में पाँच 'impulsive' लहरें (waves) और तीन 'corrective' लहरें होती हैं। यह सिद्धांत जटिल है लेकिन अगर सही से समझा जाए तो यह बाजार की दिशा का अनुमान लगाने में मदद कर सकता है।
            </p>
            <img src="https://placehold.co/600x300/4F46E5/FFFFFF?text=Elliot+Wave+Pattern" alt="इलियट वेव पैटर्न का उदाहरण" className="rounded-lg shadow-md mb-4 w-full" />
          </>
        ),
      },
      {
        id: 'volume-analysis',
        title: 'वॉल्यूम एनालिसिस',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">वॉल्यूम एनालिसिस</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              वॉल्यूम एनालिसिस, तकनीकी विश्लेषण का एक महत्वपूर्ण हिस्सा है, जो यह दर्शाता है कि किसी asset का कितना व्यापार (trade) हुआ है।
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li>बढ़ती कीमतों के साथ बढ़ता हुआ वॉल्यूम एक मजबूत trend का संकेत है।</li>
              <li>बढ़ती कीमतों के साथ घटता हुआ वॉल्यूम एक कमजोर trend का संकेत हो सकता है।</li>
              <li>वॉल्यूम में अचानक स्पाइक अक्सर किसी महत्वपूर्ण घटना (news) या reversal का संकेत देता है।</li>
            </ul>
            <img src="https://placehold.co/600x300/4F46E5/FFFFFF?text=Volume+Analysis+Chart" alt="वॉल्यूम एनालिसिस का उदाहरण" className="rounded-lg shadow-md mb-4 w-full" />
          </>
        ),
      },
    ],
  },
  {
    id: 'trading-strategies',
    title: 'ट्रेडिंग रणनीतियाँ',
    icon: <Layers size={48} />,
    lessons: [
      {
        id: 'intraday-trading',
        title: 'इंट्राडे ट्रेडिंग',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">इंट्राडे ट्रेडिंग</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              इंट्राडे ट्रेडिंग में, सभी position को एक ही ट्रेडिंग दिन के भीतर खरीदा और बेचा जाता है। इसका लक्ष्य दिन के दौरान होने वाले छोटे-छोटे price movements से लाभ कमाना है।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              <strong>उदाहरण:</strong> मान लीजिए कि किसी शेयर की कीमत सुबह ₹100 पर है, और आपको लगता है कि यह दिन में बढ़ेगी। आप सुबह ₹100 पर 100 शेयर खरीदते हैं और दोपहर में जब कीमत ₹105 हो जाती है, तो आप उन्हें बेच देते हैं। इस trade से आपको ₹500 का लाभ होता है।
            </p>
          </>
        ),
      },
      {
        id: 'swing-trading',
        title: 'स्विंग ट्रेडिंग',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">स्विंग ट्रेडिंग</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              स्विंग ट्रेडिंग में, position को कुछ दिनों से लेकर कुछ हफ्तों तक hold किया जाता है। इसका उद्देश्य मध्यम अवधि के रुझानों (trends) का लाभ उठाना है।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              <strong>उदाहरण:</strong> आप एक कंपनी के शेयर को ₹200 पर खरीदते हैं और आपको लगता है कि आने वाले कुछ हफ्तों में इसकी कीमत बढ़ेगी। आप 3 हफ्ते बाद जब शेयर की कीमत ₹225 हो जाती है, तो उसे बेच देते हैं। यह एक swing trade का उदाहरण है।
            </p>
          </>
        ),
      },
      {
        id: 'positional-trading',
        title: 'पोजिशनल ट्रेडिंग',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">पोजिशनल ट्रेडिंग</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              पोजिशनल ट्रेडिंग एक दीर्घकालिक रणनीति है जिसमें position को कई हफ्तों, महीनों या यहाँ तक कि वर्षों तक hold किया जाता है। इसका लक्ष्य बड़े रुझानों (trends) को पकड़ना है।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              इस तरह की ट्रेडिंग में कम frequent trades होते हैं और यह फंडामेंटल एनालिसिस पर ज्यादा निर्भर करती है। यह उन लोगों के लिए उपयुक्त है जिनके पास बाजार को लगातार ट्रैक करने का समय नहीं होता है।
            </p>
          </>
        ),
      },
    ],
  },
  {
    id: 'success-path',
    title: 'ट्रेडर्स के लिए सफलता की राह',
    icon: <Award size={48} />,
    lessons: [
      {
        id: 'tips-for-new-traders',
        title: 'नए ट्रेडर्स के लिए सुझाव',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">नए ट्रेडर्स के लिए सुझाव</h2>
            <ul className="list-disc list-inside space-y-2 mb-4 text-gray-700 leading-relaxed">
              <li><strong>सीखने पर ध्यान दें, कमाने पर नहीं:</strong> शुरुआत में आपका मुख्य लक्ष्य लाभ कमाना नहीं, बल्कि बाजार को समझना होना चाहिए।</li>
              <li><strong>डेमो या पेपर ट्रेडिंग करें:</strong> असली पैसे लगाने से पहले, वर्चुअल प्लेटफॉर्म पर अभ्यास करें। इससे आप बिना जोखिम के सीख सकते हैं।</li>
              <li><strong>छोटी शुरुआत करें:</strong> जब आप असली ट्रेडिंग शुरू करें, तो बहुत कम पूंजी (capital) से शुरू करें।</li>
              <li><strong>एक ट्रेडिंग प्लान बनाएं:</strong> अपनी रणनीति, जोखिम प्रबंधन और लक्ष्यों को एक प्लान में लिखें और उसका सख्ती से पालन करें।</li>
              <li><strong>अपनी भावनाओं को नियंत्रित करें:</strong> डर और लालच जैसे भावनाएं आपके सबसे बड़े दुश्मन हो सकते हैं।</li>
            </ul>
          </>
        ),
      },
      {
        id: 'strategies-for-experienced-traders',
        title: 'अनुभवी ट्रेडर्स के लिए रणनीति',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">अनुभवी ट्रेडर्स के लिए रणनीति</h2>
            <ul className="list-disc list-inside space-y-2 mb-4 text-gray-700 leading-relaxed">
              <li><strong>निरंतर सुधार करें:</strong> अपनी ट्रेडिंग जर्नल का उपयोग करके अपनी गलतियों को पहचानें और अपनी रणनीति को लगातार सुधारें।</li>
              <li><strong>बाजार की स्थितियों के अनुसार ढलें:</strong> एक ही रणनीति हर बाजार में काम नहीं करती। अपनी रणनीति को बाजार की volatility और trend के अनुसार बदलें।</li>
              <li><strong>उन्नत उपकरणों का उपयोग करें:</strong> उन्नत indicators, trading bots और data analysis tools का उपयोग करें।</li>
              <li><strong>पोर्टफोलियो का विविधीकरण करें:</strong> अपने निवेश को विभिन्न assets में फैलाएं ताकि जोखिम कम हो।</li>
            </ul>
          </>
        ),
      },
      {
        id: 'success-stories',
        title: 'सफल ट्रेडर्स की कहानियाँ',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">सफल ट्रेडर्स की कहानियाँ</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              सफल ट्रेडर्स रातों-रात अमीर नहीं बनते। वे अनुशासन, सीखने की इच्छा और धैर्य से सफलता प्राप्त करते हैं। यहाँ कुछ मुख्य बातें हैं जो उनकी कहानियों में आम हैं:
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4 text-gray-700 leading-relaxed">
              <li><strong>नुकसान को स्वीकार करना:</strong> वे जानते हैं कि नुकसान ट्रेडिंग का एक हिस्सा है। वे छोटे नुकसान को स्वीकार करके बड़े नुकसान से बचते हैं।</li>
              <li><strong>लगातार सीखना:</strong> वे बाजार के बदलते trends और नई रणनीतियों के बारे में हमेशा सीखते रहते हैं।</li>
              <li><strong>अपने प्लान पर टिके रहना:</strong> वे अपनी भावनाओं को अपने ट्रेडिंग निर्णयों को प्रभावित नहीं करने देते और अपनी योजना का पालन करते हैं।</li>
              <li><strong>छोटे से शुरू करना:</strong> कई सफल ट्रेडर्स ने बहुत कम पूंजी से शुरुआत की और धीरे-धीरे अपने ज्ञान और पूंजी को बढ़ाया।</li>
            </ul>
            <p className="text-gray-700 leading-relaxed mt-4 italic">
              "सबसे सफल ट्रेडर वे नहीं होते जो हमेशा सही होते हैं, बल्कि वे होते हैं जो सही होने पर बड़े और गलत होने पर छोटे लाभ लेते हैं।"
            </p>
          </>
        ),
      },
    ],
  },
  {
    id: 'mindset',
    title: 'सफलता और मानसिकता',
    icon: <Sparkles size={48} />,
    lessons: [
      {
        id: 'mindset-for-wealth',
        title: 'धन और सफलता की सोच',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">धन और सफलता की सोच</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              सफलता सिर्फ सही ट्रेड करने के बारे में नहीं है, बल्कि एक मजबूत मानसिक दृष्टिकोण रखने के बारे में भी है।
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4 text-gray-700 leading-relaxed">
              <li><strong>स्पष्ट लक्ष्य निर्धारित करें:</strong> अपने वित्तीय लक्ष्यों को स्पष्ट रूप से परिभाषित करें। आप क्यों ट्रेडिंग कर रहे हैं, यह जानने से आपको प्रेरणा मिलती है।</li>
              <li><strong>असफलता को सीखें:</strong> नुकसान को एक सीखने के अवसर के रूप में देखें, न कि एक हार के रूप में। हर गलती से आपको कुछ नया सीखने को मिलता है।</li>
              <li><strong>अनुशासन बनाए रखें:</strong> अपनी रणनीति पर टिके रहना और भावनाओं से बचकर चलना ही आपको लंबी अवधि में सफल बनाता है।</li>
              <li><strong>स्व-प्रेरित रहें:</strong> हर दिन अपने आप को बेहतर बनाने पर काम करें। वित्तीय ज्ञान हासिल करें और एक सकारात्मक दृष्टिकोण बनाए रखें।</li>
            </ul>
            <p className="text-gray-700 leading-relaxed mt-4">
              "जो लोग ट्रेडिंग में असफल होते हैं, वे अक्सर खुद की मानसिक सीमाओं के कारण असफल होते हैं, न कि बाजार के कारण।"
            </p>
          </>
        ),
      },
      {
        id: 'motivational-quotes',
        title: 'प्रेरक विचार और उद्धरण',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">प्रेरक विचार और उद्धरण</h2>
            <div className="grid gap-4 md:grid-cols-2 lg:grid-cols-1">
              <blockquote className="p-4 italic border-l-4 bg-gray-50 border-indigo-500 text-gray-700 rounded-lg shadow-sm">
                “बाजार आपको सिखाता है कि आप कौन हैं।”
              </blockquote>
              <blockquote className="p-4 italic border-l-4 bg-gray-50 border-indigo-500 text-gray-700 rounded-lg shadow-sm">
                “सफल ट्रेडिंग धैर्य का खेल है, गति का नहीं।”
              </blockquote>
              <blockquote className="p-4 italic border-l-4 bg-gray-50 border-indigo-500 text-gray-700 rounded-lg shadow-sm">
                “आपका सबसे बड़ा जोखिम आपका खुद का अनुशासन है।”
              </blockquote>
              <blockquote className="p-4 italic border-l-4 bg-gray-50 border-indigo-500 text-gray-700 rounded-lg shadow-sm">
                “धन कमाने का सबसे बड़ा रहस्य यह है कि यह अनुशासन और कड़ी मेहनत से आता है।”
              </blockquote>
            </div>
          </>
        ),
      },
    ],
  },
  {
    id: 'risk-management',
    title: 'जोखिम और धन प्रबंधन',
    icon: <HeartHandshake size={48} />,
    lessons: [
      {
        id: 'stop-loss-and-ts',
        title: 'स्टॉप-लॉस और ट्रेलिंग स्टॉप',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">स्टॉप-लॉस और ट्रेलिंग स्टॉप</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              <strong>स्टॉप-लॉस (Stop-Loss)</strong> एक ऐसा order है जो आपके नुकसान को सीमित करता है। यह आपके trade को स्वचालित रूप से बंद कर देता है जब कीमत एक निश्चित स्तर तक गिर जाती है।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              <strong>ट्रेलिंग स्टॉप (Trailing Stop)</strong> एक गतिशील स्टॉप-लॉस है जो कीमत के बढ़ने के साथ-साथ ऊपर चला जाता है। यह आपको लाभ सुरक्षित रखने में मदद करता है जबकि trade को और बढ़ने का मौका देता है।
            </p>
          </>
        ),
      },
      {
        id: 'position-sizing',
        title: 'पोजीशन साइजिंग',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">पोजीशन साइजिंग</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              पोजीशन साइजिंग का मतलब है यह तय करना कि एक trade में आप अपनी कुल ट्रेडिंग पूंजी का कितना प्रतिशत जोखिम में डाल रहे हैं। एक सामान्य नियम है कि एक trade में अपनी पूंजी का 1-2% से अधिक जोखिम में न डालें।
            </p>
            <p className="text-gray-700 leading-relaxed">
              यह आपके खाते को बड़े नुकसान से बचाता है और आपको लंबे समय तक बाजार में बने रहने में मदद करता है।
            </p>
          </>
        ),
      },
      {
        id: 'diversification',
        title: 'विविधीकरण (Diversification)',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">विविधीकरण</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              विविधीकरण का मतलब है अपनी निवेश पूंजी को विभिन्न assets में फैलाना। जैसे कि stocks, bonds, real estate, और commodities।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              इसका मुख्य उद्देश्य जोखिम को कम करना है। जब आप एक ही asset में सारी पूंजी नहीं लगाते हैं, तो एक asset के खराब प्रदर्शन से आपके पूरे portfolio पर कम असर पड़ता है।
            </p>
          </>
        ),
      },
      {
        id: 'risk-reward-ratio',
        title: 'जोखिम-इनाम अनुपात (Risk-Reward Ratio)',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">जोखिम-इनाम अनुपात</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              जोखिम-इनाम अनुपात यह मापता है कि किसी trade में आप संभावित नुकसान (risk) के बदले में कितना संभावित लाभ (reward) कमा सकते हैं।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              उदाहरण के लिए, 1:3 का Risk-Reward Ratio का मतलब है कि आप ₹1 का जोखिम उठाकर ₹3 का लाभ कमाने की कोशिश कर रहे हैं। सफल ट्रेडर्स आमतौर पर 1:2 या उससे बेहतर अनुपात वाले trades की तलाश करते हैं।
            </p>
          </>
        ),
      },
    ],
  },
  {
    id: 'trading-psychology',
    title: 'ट्रेडिंग मनोविज्ञान',
    icon: <Brain size={48} />,
    lessons: [
      {
        id: 'emotions',
        title: 'डर और लालच पर काबू पाना',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">डर और लालच पर काबू पाना</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              ट्रेडिंग में, भावनाएं (emotions) आपके सबसे बड़े दुश्मन हो सकती हैं।
            </p>
            <ul className="list-disc list-inside space-y-2 mb-4">
              <li><strong>लालच (Greed):</strong> जब आप छोटे लाभ से संतुष्ट नहीं होते और बड़े लाभ की उम्मीद में trade को hold करते हैं, जिससे अक्सर नुकसान होता है।</li>
              <li><strong>डर (Fear):</strong> जब आप नुकसान से डरकर जल्दी trade बंद कर देते हैं या सही opportunity चूक जाते हैं।</li>
            </ul>
            <p className="text-gray-700 leading-relaxed">
              सफल ट्रेडिंग के लिए इन भावनाओं को पहचानना और नियंत्रित करना आवश्यक है।
            </p>
          </>
        ),
      },
      {
        id: 'discipline-and-journaling',
        title: 'अनुशासन और ट्रेडिंग जर्नल',
        content: (
          <>
            <h2 className="text-2xl font-bold mb-4 text-gray-800">अनुशासन और ट्रेडिंग जर्नल</h2>
            <p className="text-gray-700 leading-relaxed mb-4">
              <strong>अनुशासन (Discipline)</strong> का मतलब है अपनी ट्रेडिंग योजना का पालन करना, भले ही बाजार आपकी भावनाओं को चुनौती दे।
            </p>
            <p className="text-gray-700 leading-relaxed mb-4">
              <strong>ट्रेडिंग जर्नल (Trading Journal)</strong> में अपने सभी ट्रेड्स का रिकॉर्ड रखना एक शक्तिशाली उपकरण है। इसमें आप यह नोट करते हैं कि आपने क्यों trade किया, आपका स्टॉप-लॉस कहाँ था, और आपने कैसा महसूस किया। यह आपको अपनी गलतियों से सीखने और अपनी रणनीति को सुधारने में मदद करता है।
            </p>
          </>
        ),
      },
    ],
  },
];

// Main App component with a beautiful and modern design
export default function App() {
  const [currentPage, setCurrentPage] = useState('home');
  const [currentCategory, setCurrentCategory] = useState(null);
  const [currentLesson, setCurrentLesson] = useState(null);

  useEffect(() => {
    // Add the manifest link to the head of the document
    const link = document.createElement('link');
    link.rel = 'manifest';
    link.href = '/manifest.json';
    document.head.appendChild(link);
    return () => {
      document.head.removeChild(link);
    };
  }, []);

  // Function to render the correct page based on state
  const renderPage = () => {
    switch (currentPage) {
      case 'home':
        return (
          <div className="p-4 sm:p-6 lg:p-8">
            <h1 className="text-3xl sm:text-4xl font-extrabold text-center mb-4 text-white">ट्रेडिंग और इन्वेस्टिंग सीखें</h1>
            <p className="text-center text-indigo-100 mb-8 max-w-xl mx-auto">
              यह वित्तीय बाजारों में सफल होने के लिए आपकी comprehensive guide है। नीचे दिए गए sections में से चुनें और सीखना शुरू करें।
            </p>
            <div className="grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
              {categories.map((category) => (
                <button
                  key={category.id}
                  onClick={() => {
                    setCurrentCategory(category);
                    setCurrentPage('category');
                  }}
                  className="bg-white rounded-xl shadow-xl p-6 flex flex-col items-center text-center hover:bg-gray-50 transition-all duration-300 transform hover:scale-105"
                >
                  <div className="text-indigo-600 mb-3 w-16 h-16 flex items-center justify-center">
                    {category.icon}
                  </div>
                  <h2 className="text-xl font-semibold text-gray-800">{category.title}</h2>
                </button>
              ))}
            </div>
          </div>
        );
      case 'category':
        return (
          <div className="p-4 sm:p-6 lg:p-8">
            <button
              onClick={() => {
                setCurrentPage('home');
                setCurrentCategory(null);
              }}
              className="flex items-center text-indigo-200 hover:text-white font-medium mb-6 transition-colors duration-200"
            >
              <ChevronLeft className="w-5 h-5 mr-1" />
              <span>होम</span>
            </button>
            <h1 className="text-3xl font-bold mb-6 text-white">{currentCategory.title}</h1>
            <div className="space-y-4">
              {currentCategory.lessons.map((lesson) => (
                <button
                  key={lesson.id}
                  onClick={() => {
                    setCurrentLesson(lesson);
                    setCurrentPage('lesson');
                  }}
                  className="w-full bg-white rounded-xl shadow-md p-5 text-left flex items-center hover:bg-gray-50 transition-all duration-300 transform hover:scale-[1.01]"
                >
                  <div className="flex-grow">
                    <h2 className="text-lg font-semibold text-gray-800">{lesson.title}</h2>
                  </div>
                  <ChevronLeft className="w-5 h-5 transform rotate-180 text-gray-400" />
                </button>
              ))}
            </div>
          </div>
        );
      case 'lesson':
        return (
          <div className="p-4 sm:p-6 lg:p-8">
            <button
              onClick={() => {
                setCurrentPage('category');
                setCurrentLesson(null);
              }}
              className="flex items-center text-indigo-200 hover:text-white font-medium mb-6 transition-colors duration-200"
            >
              <ChevronLeft className="w-5 h-5 mr-1" />
              <span>{currentCategory.title}</span>
            </button>
            <div className="bg-white rounded-xl shadow-lg p-6 sm:p-8 lg:p-10">
              {currentLesson.content}
            </div>
          </div>
        );
      default:
        return null;
    }
  };

  return (
    <div className="min-h-screen font-sans antialiased text-gray-900 bg-gradient-to-br from-indigo-500 to-purple-600">
      <div className="max-w-4xl mx-auto py-8">
        {renderPage()}
      </div>
    </div>
  );
}