# WatchGuard6S Project

## 🚀 Project Overview
### Vision
- To revolutionize solar farm security and maintenance through cutting-edge technology.
- Ensuring sustainable energy production with unmatched safety, efficiency, and precision.
### Idea
- AI-powered robotic system integrating security, surveillance, and real-time monitoring.
- Detects environmental hazards, optimizes panel performance and automates maintenance.
- Uses high-resolution cameras, AI analytics, and
thermal imaging for 24/7 security.
### Technology & innovativeness
- Advanced camera systems
- AI-Driven analytics
- Multifunctional sensors
- Autonomous operation

<br>
<br>


## 👥 Teams

### 🧠 AI Team
- **Responsibilities**: Algorithm development, machine learning, computer vision
- **Directory**: `/AI_team/`
- **Tech stack**: Python, TensorFlow/PyTorch, OpenCV, ROS 2...

### ⚡ ECE Team
- **Responsibilities**: Circuit design, firmware, sensors, communication systems
- **Directory**: `/ECE_team/`
- **Tech stack**: C/C++, Arduino/ESP32, EasyEDA, ROS 2...

### 🔧 MECH Team
- **Responsibilities**: Mechanical design, robot chassis, actuators
- **Directory**: `/MECH_team/`
- **Tech stack**: SolidWorks, AutoCAD, 3D printing...

<br>
<br>

## 📁 Project Structure
```
├── AI_team/          # AI/ML code and models
├── ECE_team/         # Firmware and PCB designs  
├── MECH_team/        # CAD files and mechanical designs
├── integration/      # System integration and testing
├── docs/             # Documentation
└── resources/        # Shared resources
```

<br><br>

## 🔄 Workflow 

### 🌳 Branch Structure

```
master (main)
├── ai-team (long-running)
│   ├── ai/feature-object-detection
│   └── ...
├── ece-team (long-running)
│   ├── ece/feature-motor-control
│   └── ...
└── mech-team (long-running)
    ├── mech/feature-chassis-design
    └── ...
```

### 📋 Branch Types

#### 1. Main Branches
- **`master`**: stable branch
- **`ai-team`**: AI team's integration branch
- **`ece-team`**: ECE team's integration branch  
- **`mech-team`**: MECH team's integration branch

#### 2. Feature Branches
- **`ai/feature-name`**: AI team features branch
- **`ece/feature-name`**: ECE team features branch
- **`mech/feature-name`**: MECH team features branch


### Naming Convention
- **`Branches`**: `ai/object-detection`, `ece/motor-control`, `mech/chassis-design`
- **`Commits`**: `feat:`, `fix:`, `docs:`, `test:`

<br>

### 🔄 Workflow Process

#### Phase 1: Initial Setup
```bash
# 1. Clone repository (all team members)
git clone https://github.com/thanhphucse/watchGuard6S_Snetel_PSG.git
cd watchGuard6S_Snetel_PSG
git remote add origin https://github.com/thanhphucse/watchGuard6S_Snetel_PSG.git

# 2. Create and push team branches (Team leader only)

# (AI team leader)
git checkout -b ai-team
git push -u origin ai-team

# (ECE team leader)
git checkout -b ece-team
git push -u origin ece-team

# (MECH team leader)
git checkout -b mech-team
git push -u origin mech-team
```
<br>

#### Phase 2: Team Development Workflow

##### 1.  For AI Team Members:
```bash
# 1. Start from team branch
git checkout ai-team
git pull origin ai-team

# 2. Create feature branch
git checkout -b ai/feature-object-detection

# 3. Work on feature
# ... make changes ...
git add .
git commit -m "feat: implement YOLO object detection"

# 4. Push feature branch
git push -u origin ai/feature-object-detection

# 5. Create Pull Request: ai/feature-object-detection → ai-team
# 6. After review and approval, merge to ai-team
# 7. Delete feature branch after merge
git checkout ai-team
git branch -d ai/feature-object-detection
git push origin --delete ai/feature-object-detection
```

##### 2. For ECE Team Members:
```bash
# 1. Start from team branch
git checkout ece-team
git pull origin ece-team

# 2. Create feature branch
git checkout -b ece/feature-motor-control

# 3. Work on feature
# ... make changes ...
git add .
git commit -m "feat: add PWM motor control system"

# 4. Push feature branch
git push -u origin ece/feature-motor-control

# 5. Create Pull Request: ece/feature-motor-control → ece-team
# 6. After review and approval, merge to ece-team
# 7. Delete feature branch after merge
git checkout ece-team
git branch -d ece/feature-motor-control
git push origin --delete ece/feature-motor-control
```

##### 3. For MECH Team Members:
```bash
# 1. Start from team branch
git checkout mech-team
git pull origin mech-team

# 2. Create feature branch
git checkout -b mech/feature-chassis-design

# 3. Work on feature
# ... make changes ...
git add .
git commit -m "feat: design robot chassis CAD files"

# 4. Push and create PR to mech-team
git push -u origin mech/feature-chassis-design

# 5. Create Pull Request: mech/feature-chassis-design → mech-team
# 6. After review and approval, merge to mech-team
# 7. Delete feature branch after merge
git checkout mech-team
git branch -d mech/feature-chassis-design
git push origin --delete mech/feature-chassis-design
```

<br>

#### Phase 3: Integration to Master

##### Team Lead Integration Process (this process for AI team, similarly with ECE and MECH team):
```bash
# When team is ready to integrate to master
# 1. Ensure team branch is up to date
git checkout ai-team
git pull origin ai-team

# 2. Update with latest master changes
git checkout master
git pull origin master
git checkout ai-team
git merge master

# 3. Resolve conflicts if any
# 4. Push updated team branch
git push origin ai-team

# 5. Create Pull Request: ai-team → master
# 6. Require reviews from other team leads
# 7. After approval, merge to master
```
<br>

## 🤝 Collaboration Guidelines
- Each team can work independently within their directory
- Use Issues to track tasks and bugs
- Pull Requests require at least 1 review from another team

## 📞 Contact
- **AI Team Lead**: [Name]
- **ECE Team Lead**: [Name] 
- **MECH Team Lead**: [Name]