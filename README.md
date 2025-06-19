# Q-A
Study
from fpdf import FPDF

questions_and_answers = [
    ("Tell me about yourself.",
     "Hello, my name is [Your Name]. I recently completed my B.Tech in Information Technology from [Your College]. During my studies, I developed a strong interest in system administration and networking. I have basic knowledge of Windows and Linux operating systems, networking concepts, and tools like SQL and Python. I’ve also worked on a few college projects where I configured networks and managed system settings. I’m a quick learner, enjoy troubleshooting, and am excited to start my career as a System Engineer."),
    
    ("What is a System Engineer?",
     "A System Engineer is responsible for designing, managing, and maintaining IT infrastructure. This includes configuring servers, installing and updating operating systems, managing networks, and ensuring system security and performance. They also troubleshoot hardware and software issues to keep systems running smoothly."),
    
    ("What operating systems are you familiar with?",
     "I am familiar with Windows and Linux operating systems. I’ve used both during my college projects and labs. I know how to use basic commands in Linux and manage files, users, and processes. I’m also comfortable with tasks like software installation and system configuration in Windows."),
    
    ("What is the difference between RAM and ROM?",
     "RAM (Random Access Memory) is a type of volatile memory used to store data temporarily while the computer is running. It helps in fast access and smooth performance. ROM (Read-Only Memory) is non-volatile memory that stores permanent data, like the BIOS, which is needed during system startup."),
    
    ("What are IP address and MAC address?",
     "An IP address is a unique address assigned to a device on a network to identify it and allow communication. A MAC address is a hardware address that identifies a device’s network interface card (NIC). IP addresses can change, but MAC addresses are permanent."),
    
    ("What is the difference between a switch and a router?",
     "A switch connects devices within the same network and forwards data based on MAC addresses. A router connects different networks and forwards data based on IP addresses. Routers are used to connect to the internet, while switches are used within local networks."),
    
    ("What is DNS?",
     "DNS stands for Domain Name System. It is used to convert human-readable domain names like www.google.com into IP addresses that computers use to identify each other on the network."),
    
    ("What is the Blue Screen of Death (BSOD)?",
     "BSOD is a critical system error in Windows that occurs when the operating system encounters a fatal issue, such as a hardware failure or driver conflict. It usually requires a restart and troubleshooting to identify the cause."),
    
    ("What are your strengths?",
     "My strengths are that I’m a quick learner, detail-oriented, and good at problem-solving. I also enjoy troubleshooting and learning new technologies, which makes me well-suited for a System Engineer role."),
    
    ("Why do you want to work as a System Engineer?",
     "I enjoy working with computer systems and solving technical issues. I’m interested in system infrastructure, and I find it exciting to configure and maintain systems to keep everything running smoothly. This role matches my skills and passion for IT.")
]

pdf = FPDF()
pdf.add_page()
pdf.set_font("Arial", 'B', 14)
pdf.cell(200, 10, txt="System Engineer Interview Questions & Answers for Freshers", ln=True, align='C')
pdf.ln(10)
pdf.set_font("Arial", size=12)

for i, (q, a) in enumerate(questions_and_answers, 1):
    pdf.set_font("Arial", 'B', 12)
    pdf.multi_cell(0, 10, f"{i}. {q}")
    pdf.set_font("Arial", size=12)
    pdf.multi_cell(0, 10, f"Answer: {a}")
    pdf.ln(2)

pdf.output("System_Engineer_Interview_QnA_Fresher.pdf")
