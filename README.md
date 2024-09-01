

## เว็บแอปพลิเคชัน Strapi 
เว็บแอปพลิเคชัน Strapi เป็น headless CMS (content management system) คือ การตัดส่วนหน้าบ้านออกไป มีเพียงส่วนของ API และหลังบ้าน ทำให้นักพัฒนาการทำงานได้สะดวก รวดเร็ว ยืดหยุ่น ช่วยสร้างและจัดการ API ได้อย่างง่าย ช่วยให้การบริหารจัดการข้อมูลและเชื่อมโยงการทำงานระหว่าง frontend และ backend ทำได้อย่างปลอดภัย และทำงานร่วมกับ framework ส่วนใหญ่ได้อย่างเช่น React และ Node

![enter image description here](https://miro.medium.com/v2/resize:fit:1100/format:webp/0*8eHo2OyIhH9FuIF3.png)
**Ref** : https://medium.com/@themaxaboy/ ออกแบบสร้าง APIs แบบโคตรเร็ว, จัดการเนื้อหาแบบโคตรง่าย ด้วย Strapi Headless CMS by Max Veerapat Kumchom



## กรณีการใช้งาน 
- ใช้สำหรับจัดการข้อมูลเนื้อหาต่างๆ เช่น ใช้จัดการบทความ, หมวดหมู่, ผู้ใช้บนบล็อก
- ใช้สำหรับการสร้าง API เพื่อเข้าถึงข้อมูลในรูปแบบที่แตกต่างกัน 
- ใช้สำหรับการสร้าง Web Application และ Application


## มีองค์ประกอบใดบ้าง?
   องค์ประกอบหลักของ Strapi มีทั้งหมด 7 ส่วน ดังนี้ 
 - **Content Manager** เป็นส่วนที่เป็นปลั๊กอินหลักของ Strapi ในส่วนนี้จะช่วยในการออกแบบโครงสร้างข้อมูล ซึ่งประกอบด้วย collection types (multiple entries) และ single type (one default entry per available single type) ในแต่ละประเภทจะสามารถสร้าง types ไว้ล่วงหน้าก่อนนำไปใช้ใน content-type Builder โดยแอดมินสามารถสร้าง จัดการ และเผยแพร่ content ได้ ![](https://docs.strapi.io/img/assets/content-manager/content-manager_list-view.png)

 - **Content-type Builder** เป็นปลั๊กอินหลักของ Strapi ในส่วนนี้เป็นระบบจัดการเนื้อหา แอดมินสามารถสร้าง และจัดการ content-type และ component (data structure ที่สามารถใช้ได้ multiple collection types และ single types) และในแต่ละประเภทจะแสดง content-type และ component  ทั้งหมดที่ถูกสร้างขึ้น ![](https://docs.strapi.io/img/assets/content-type-builder/content-types-builder.png)

 - **Media Library** แสดง assets ทั้งหมดที่อัปโหลดบนแอปพลิเคชันและสามารถใส่ใน content-type ได้โดยผ่าน content manager และสามารถอัปโหลดเนื้อหาประเภท images, videos, audio files, PDFs, or GIFs ได้เป็นต้น![](https://docs.strapi.io/img/assets/media-library/media-library_filters.png)

 - **Releases** จะเปิดใช้งานให้ content managers จัดการการเผยแพร่ entries โดยสามารถมี entries จากต่าง content type หรือ จากตำแหน่งอื่นๆได้ ![](https://docs.strapi.io/img/assets/releases/releases-overview.png)

 - **Users, Roles & Permission** เป็นส่วนที่จัดการ roles และสิทธิ์การเข้าถึงของ users โดยสามารถใช้ฟีเจอร์ Role Based Access Control (RBAC) หรือ Users & Permissions plugin ก็ได้เช่นกัน โดยทั้งสองจะอยู่ใน setting บน admin panel ![](https://docs.strapi.io/img/assets/users-permissions/users-roles-permissions-settings.png)

 - **Plugins** ตัว Strapi สร้างขึ้นจากปลั๊กอินหลายๆประเภท โดยมี pre-installed plugins ดังภาพ และสามารถเพิ่มปลั๊กอินตัวอื่นๆได้ใน Marketplace ด้านซ้ายมือ![](https://docs.strapi.io/img/assets/plugins/plugins-settings.png)
   
 - **Setting**  เป็นส่วนที่รวมข้อมูลการตั้งค่าที่จําเป็นทั้งหมด และวิธีที่ admin ใช้งานและจัดการแอปพลิเคชัน Strapi จะมี 4 ส่วนย่อย ดังนี้ global setting, administration panel, email plugin and user & permission plugin  ![](https://docs.strapi.io/img/assets/settings/settings_custom-logo.png)
**Ref** : https://docs.strapi.io/user-docs/intro
 
## ไฟล์ .gitignore 
ไฟล์ .gitignore มีไว้เพื่อให้ Git ไม่สนใจไฟล์และโฟลเดอร์ที่อยู่ในไฟล์ .gitignore ซึ่งภายในไฟล์นั้นจะมีไฟล์ที่ไม่ควรแชร์กับผู้อื่น ไฟล์ที่สามารถสร้างใหม่ได้ หรือไฟล์ที่ขนาดใหญ่ เพื่อให้สะอาด ปลอดภัย และง่ายต่อการจัดการ

## ขั้นตอนการติดตั้ง Strapi ด้วย CLI 
**ความต้องการระบบ**
 - ติดตั้ง Node.js version 18 และ version 20
 - npm version 6 ขึ้นไป
 
**การติดตั้ง Project Strapi**

 1. เปิด ไฟล์ Project Strapi ใน Terminal 
 2. ใช้คำสั่ง
	`npx create-strapi-app@latest my-project`
3. เลือกการติดตั้งแบบ Quickstart
4. กรอกข้อมูล register admin เพื่อเช้าใช้งานระบบ 

**การรัน Project Strapi**

ใช้คำสั่ง `npm  run  develop`
 
 Ref : https://docs.strapi.io/dev-docs/installation/cli

## การนำเว็บแอปพลิเคชันขึ้นให้บริการบน AWS
1.สร้าง repository และนำ Project Strapi ขึ้นบน Git
2.สร้าง EC2 instance บน AWS ดังนี้

 **Application and OS Images** : Ubuntu Server 22.04 LTS (HVM), SSD Volume Type
  **Instance type** : t2.medium
  **Network setting** : create security group
-   Type:  `SSH`,  Protocol:  `TCP`,  Port Range  `22`,  Source:  `::/0`
-   Type:  `HTTP`,  Protocol:  `TCP`,  Port Range  `80`,  Source:  `0.0.0.0/0, ::/0`
-   Type:  `HTTPS`,  Protocol:  `TCP`,  Port Range  `443`,  Source:  `0.0.0.0/0, ::/0`
-   Type:  `Custom TCP Rule`,  Protocol:  `TCP`,  Port Range  `1337`,  Source:  `0.0.0.0/0`

3. เข้า EC2 instance ที่สร้างไว้
4. อัพเดตระบบ โดยใช้คำสั่ง
 `curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
 `  และ
 `sudo apt install -y nodejs` และ
 `node -v && npm -v` 
 5. สร้าง directory .npm-global และ Set path มา directory สำหรับ node_modules โดยใช้คำสั่ง
 `cd ~`  
 `mkdir ~/.npm-global`  
 `npm config set prefix '~/.npm-global'`
 6. สร้าง หรือแก้ไขไฟล์ ~/.profile
 `sudo nano ~/.profile` 
 7. เพิ่ม `export PATH=~/.npm-global/bin:$PATH` ไว้บรรดทัดด้านสุดท้าย
 8. ใช้คำสั่ง  `source ~/.profile` เพื่ออัปเดต system variables
 9. เช็คว่ามี Git หรือไม่โดย `git --version` หากไม่มี Git  ติดตั้ง Git โดยใช้คำสั่ง 
  `sudo apt install git -y`
  10. Clone Project Strapi จาก Git โดยใช้คำสั่ง
   `git clone <url repo>`
  11. cd ไปในไฟล์ project 
  12. ติดตั้ง library โดยใช้คำสั่ง
  `npm install`
  13. สร้างไฟล์ .env โดยใช้คำสั่ง `touch .env` และ copy เนื้อหาในไฟล์ project จากเครื่อง local ใส่ในไฟล์ที่พึ่งสร้างขึ้นแล้ะเพิ่มบรรทัดสุดท้าย ดังนี้ `NODE_ENV=production`
  14. รัน Project Strapi โดยใช้คำสั่ง `npm  run  develop`

 **Ref** : https://docs.strapi.io/dev-docs/deployment/amazon-aws

