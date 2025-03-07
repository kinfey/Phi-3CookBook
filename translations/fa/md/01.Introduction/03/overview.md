در زمینه Phi-3-mini، استنتاج به فرآیندی اشاره دارد که طی آن مدل برای پیش‌بینی یا تولید خروجی‌ها بر اساس داده‌های ورودی استفاده می‌شود. اجازه دهید جزئیات بیشتری درباره Phi-3-mini و قابلیت‌های استنتاج آن ارائه کنم.

Phi-3-mini بخشی از سری مدل‌های Phi-3 است که توسط مایکروسافت عرضه شده‌اند. این مدل‌ها طراحی شده‌اند تا تعریف جدیدی از قابلیت‌های مدل‌های کوچک زبانی (SLM) ارائه دهند.

در اینجا نکات کلیدی درباره Phi-3-mini و قابلیت‌های استنتاج آن آورده شده است:

## **مروری بر Phi-3-mini:**
- Phi-3-mini دارای اندازه پارامتری ۳.۸ میلیارد است.
- این مدل نه تنها روی دستگاه‌های محاسباتی سنتی بلکه روی دستگاه‌های لبه‌ای مانند دستگاه‌های موبایل و دستگاه‌های اینترنت اشیا نیز قابل اجرا است.
- عرضه Phi-3-mini این امکان را برای افراد و شرکت‌ها فراهم می‌کند تا SLMها را روی سخت‌افزارهای مختلف، به‌ویژه در محیط‌های با منابع محدود، مستقر کنند.
- این مدل شامل فرمت‌های مختلفی است، از جمله فرمت سنتی PyTorch، نسخه کوانتیده‌شده فرمت gguf و نسخه کوانتیده‌شده مبتنی بر ONNX.

## **دسترسی به Phi-3-mini:**
برای دسترسی به Phi-3-mini، می‌توانید از [Semantic Kernel](https://github.com/microsoft/SemanticKernelCookBook?WT.mc_id=aiml-138114-kinfeylo) در یک اپلیکیشن Copilot استفاده کنید. Semantic Kernel به‌طور کلی با Azure OpenAI Service، مدل‌های متن‌باز در Hugging Face و مدل‌های محلی سازگار است.  
همچنین می‌توانید از [Ollama](https://ollama.com) یا [LlamaEdge](https://llamaedge.com) برای فراخوانی مدل‌های کوانتیده استفاده کنید. Ollama به کاربران فردی اجازه می‌دهد مدل‌های کوانتیده مختلف را فراخوانی کنند، در حالی که LlamaEdge امکان دسترسی به مدل‌های GGUF را در پلتفرم‌های مختلف فراهم می‌کند.

## **مدل‌های کوانتیده:**
بسیاری از کاربران ترجیح می‌دهند برای استنتاج محلی از مدل‌های کوانتیده استفاده کنند. به عنوان مثال، می‌توانید به‌طور مستقیم Ollama run Phi-3 را اجرا کنید یا آن را به صورت آفلاین با استفاده از یک Modelfile پیکربندی کنید. Modelfile مسیر فایل GGUF و فرمت prompt را مشخص می‌کند.

## **امکانات هوش مصنوعی تولیدی:**
ترکیب مدل‌های SLM مانند Phi-3-mini امکانات جدیدی را برای هوش مصنوعی تولیدی فراهم می‌کند. استنتاج تنها گام اول است؛ این مدل‌ها می‌توانند برای وظایف مختلف در محیط‌های با منابع محدود، محدودیت زمانی و هزینه‌ای استفاده شوند.

## **باز کردن قفل هوش مصنوعی تولیدی با Phi-3-mini: راهنمای استنتاج و استقرار**  
یاد بگیرید چگونه از Semantic Kernel، Ollama/LlamaEdge و ONNX Runtime برای دسترسی و استنتاج مدل‌های Phi-3-mini استفاده کنید و امکانات هوش مصنوعی تولیدی را در سناریوهای مختلف کاربردی کشف کنید.

**ویژگی‌ها**  
استنتاج مدل phi3-mini در:

- [Semantic Kernel](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/semantickernel?WT.mc_id=aiml-138114-kinfeylo)
- [Ollama](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/ollama?WT.mc_id=aiml-138114-kinfeylo)
- [LlamaEdge WASM](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/wasm?WT.mc_id=aiml-138114-kinfeylo)
- [ONNX Runtime](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/onnx?WT.mc_id=aiml-138114-kinfeylo)
- [iOS](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/ios?WT.mc_id=aiml-138114-kinfeylo)

به طور خلاصه، Phi-3-mini به توسعه‌دهندگان اجازه می‌دهد فرمت‌های مختلف مدل را بررسی کرده و از هوش مصنوعی تولیدی در سناریوهای مختلف کاربردی بهره ببرند.

**سلب مسئولیت**:  
این سند با استفاده از خدمات ترجمه ماشینی مبتنی بر هوش مصنوعی ترجمه شده است. در حالی که ما برای دقت تلاش می‌کنیم، لطفاً توجه داشته باشید که ترجمه‌های خودکار ممکن است حاوی خطاها یا نادقتی‌هایی باشند. سند اصلی به زبان اصلی آن باید به عنوان منبع معتبر در نظر گرفته شود. برای اطلاعات حیاتی، ترجمه انسانی حرفه‌ای توصیه می‌شود. ما هیچ مسئولیتی در قبال سوءتفاهم‌ها یا برداشت‌های نادرست ناشی از استفاده از این ترجمه نداریم.