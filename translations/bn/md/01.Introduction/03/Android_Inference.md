# **Android-এ Phi-3-এর ইনফারেন্স**

চলুন দেখি কিভাবে আপনি Android ডিভাইসগুলিতে Phi-3-mini ব্যবহার করে ইনফারেন্স করতে পারেন। Phi-3-mini হল Microsoft-এর একটি নতুন মডেল সিরিজ যা বড় ভাষাগত মডেলগুলোকে (LLMs) এজ ডিভাইস এবং IoT ডিভাইসে ডেপ্লয় করার সুযোগ দেয়।

## সেমান্টিক কার্নেল এবং ইনফারেন্স

[সেমান্টিক কার্নেল](https://github.com/microsoft/semantic-kernel) একটি অ্যাপ্লিকেশন ফ্রেমওয়ার্ক যা Azure OpenAI Service, OpenAI মডেল এবং এমনকি লোকাল মডেলের সাথে সামঞ্জস্যপূর্ণ অ্যাপ্লিকেশন তৈরি করতে সাহায্য করে। যদি আপনি সেমান্টিক কার্নেলে নতুন হন, আমরা আপনাকে [সেমান্টিক কার্নেল কুকবুক](https://github.com/microsoft/SemanticKernelCookBook?WT.mc_id=aiml-138114-kinfeylo) দেখার পরামর্শ দিচ্ছি।

### সেমান্টিক কার্নেল ব্যবহার করে Phi-3-mini-তে অ্যাক্সেস করা

আপনি এটি সেমান্টিক কার্নেলের Hugging Face Connector-এর সাথে একত্রিত করতে পারেন। এই [নমুনা কোড](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/semantickernel?WT.mc_id=aiml-138114-kinfeylo) দেখুন।

ডিফল্টভাবে, এটি Hugging Face-এর মডেল ID-এর সাথে সামঞ্জস্যপূর্ণ। তবে, আপনি একটি লোকালভাবে তৈরি করা Phi-3-mini মডেল সার্ভারের সাথেও সংযোগ করতে পারেন।

### Ollama বা LlamaEdge দিয়ে কোয়ান্টাইজড মডেল চালানো

অনেক ব্যবহারকারী মডেলগুলো লোকালভাবে চালানোর জন্য কোয়ান্টাইজড মডেল ব্যবহার করতে পছন্দ করেন। [Ollama](https://ollama.com/) এবং [LlamaEdge](https://llamaedge.com) ব্যক্তিগত ব্যবহারকারীদের বিভিন্ন কোয়ান্টাইজড মডেল চালানোর সুযোগ দেয়:

#### Ollama

আপনি সরাসরি `ollama run Phi-3` চালাতে পারেন বা `Modelfile` তৈরি করে আপনার `.gguf` ফাইলের পথ কনফিগার করতে পারেন।

```gguf
FROM {Add your gguf file path}
TEMPLATE \"\"\"<|user|> .Prompt<|end|> <|assistant|>\"\"\"
PARAMETER stop <|end|>
PARAMETER num_ctx 4096
```

[নমুনা কোড](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/ollama?WT.mc_id=aiml-138114-kinfeylo)

#### LlamaEdge

যদি আপনি একই সাথে ক্লাউড এবং এজ ডিভাইসে `.gguf` ফাইল ব্যবহার করতে চান, তাহলে LlamaEdge একটি চমৎকার পছন্দ। শুরু করার জন্য এই [নমুনা কোড](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/wasm?WT.mc_id=aiml-138114-kinfeylo) দেখুন।

### Android ফোনে ইনস্টল এবং চালানো

1. **MLC Chat অ্যাপ ডাউনলোড করুন** (ফ্রি) Android ফোনের জন্য।  
2. APK ফাইল (১৪৮MB) ডাউনলোড করে আপনার ডিভাইসে ইনস্টল করুন।  
3. MLC Chat অ্যাপ চালু করুন। আপনি একটি AI মডেলের তালিকা দেখতে পাবেন, যেখানে Phi-3-mini অন্তর্ভুক্ত রয়েছে।  

সারাংশে, Phi-3-mini এজ ডিভাইসে জেনারেটিভ AI-এর জন্য উত্তেজনাপূর্ণ সম্ভাবনা উন্মোচন করে, এবং আপনি Android-এ এর ক্ষমতাগুলো অন্বেষণ শুরু করতে পারেন।  

**অস্বীকৃতি**:  
এই নথি মেশিন-ভিত্তিক কৃত্রিম বুদ্ধিমত্তা অনুবাদ পরিষেবা ব্যবহার করে অনুবাদ করা হয়েছে। আমরা যথাসম্ভব সঠিক অনুবাদের জন্য চেষ্টা করি, তবে অনুগ্রহ করে মনে রাখবেন যে স্বয়ংক্রিয় অনুবাদে ত্রুটি বা অসংগতি থাকতে পারে। নথিটির মূল ভাষায় লেখা সংস্করণটিকেই প্রামাণিক উৎস হিসেবে বিবেচনা করা উচিত। গুরুত্বপূর্ণ তথ্যের জন্য পেশাদার মানব অনুবাদের পরামর্শ দেওয়া হচ্ছে। এই অনুবাদ ব্যবহারের ফলে কোনো ভুল বোঝাবুঝি বা ভুল ব্যাখ্যার জন্য আমরা দায়ী নই।