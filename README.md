pythonimport os
import time
import random

# إحداثيات مكان المورد على شاشة التابلت (كمثال)
# يمكنك تغييرها حسب موقع المورد في خريطة اللعبة
X_POSITION = 500  
Y_POSITION = 750  

print("بدء تشغيل بوت الفارم التجريبي...")

try:
    while True:
        # إرسال أمر نقرة (Tap) إلى شاشة الأندرويد عبر نظام التابلت الداخلي
        os.system(f"input tap {X_POSITION} {Y_POSITION}")
        print(f"تم النقر على الإحداثيات: ({X_POSITION}, {Y_POSITION})")
        
        # وقت انتظار عشوائي بين 8 إلى 12 ثانية حتى يكتمل الجني ويفلت من الرصد التلقائي
        wait_time = random.uniform(8.0, 12.0)
        time.sleep(wait_time)
        
except KeyboardInterrupt:
    print("تم إيقاف البوت بنجاح.")
