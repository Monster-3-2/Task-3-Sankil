# Task-3-Sankil
## 🤖 Project 3: Tech Stack Recommender (Content-Based Filtering)

**File:** `decodelabs3.py`

### Overview
An **AI-powered career recommendation engine** using **TF-IDF** (Term Frequency-Inverse Document Frequency) and **Cosine Similarity**. Users enter their skills and receive career path recommendations.

### What It Does
1. **Skill Input**: Collects at least 3 user skills (with validation)
2. **Vocabulary Building**: Extracts unique skills from 15+ job role profiles
3. **TF-IDF Vectorization**: Converts skill sets into numerical vectors
4. **Cosine Similarity Scoring**: Compares user skills against job role profiles
5. **Ranking & Filtering**: Returns top N recommendations with match percentages
6. **Visual Display**: Shows results with emoji medals and progress bars

### Key Concepts Covered
- ✅ Content-based filtering (recommendation systems)
- ✅ TF-IDF vectorization
- ✅ Cosine similarity scoring
- ✅ Cold-start problem mitigation (minimum 3 skill input)
- ✅ User interaction & onboarding

### Available Job Roles (15 Total)
- Data Scientist
- Data Engineer
- Machine Learning Engineer
- Backend Developer
- Frontend Developer
- Full Stack Developer
- DevOps Engineer
- Cloud Architect
- Cybersecurity Analyst
- AI Research Scientist
- NLP Engineer
- Mobile Developer
- Database Administrator
- Systems Administrator
- Blockchain Developer

### Available Skills (Sample)
```
python, java, javascript, sql, machine learning, deep learning, aws, docker,
kubernetes, react, nodejs, linux, security, nlp, data analysis, tensorflow,
pandas, scikit-learn, pytorch, azure, gcp, ci/cd, kubernetes, ...
```

### Requirements
```
(Built-in libraries only - no external dependencies!)
- math
- collections
```

### Usage
```bash
python decodelabs3.py
```

### Interactive Example
```
🚀  Welcome to the Tech Stack Recommender!
   Powered by TF-IDF + Cosine Similarity
=====================================

Enter at least 3 skills (one per line). Type 'done' when finished.

  Skill 1: python
  Skill 2: machine learning
  Skill 3: tensorflow
  (You can add more or type 'done' to get recommendations)
  Skill 4: deep learning
  Skill 5: done

How many recommendations would you like? [default: 3]: 5

🤖  TECH STACK RECOMMENDER  —  DecodeLabs
================================================
  Your Skills : python, machine learning, tensorflow, deep learning
------------------------------------------------
  TOP RECOMMENDED CAREER PATHS
------------------------------------------------
  🥇  AI Research Scientist
      Match: 75.23%  ██████████████████████████████
      Skills needed: python, machine learning, deep learning, mathematics, statistics...

  🥈  Machine Learning Engineer
      Match: 72.15%  ███████████████████████████
      Skills needed: python, machine learning, deep learning, tensorflow, pytorch...

  🥉  Data Scientist
      Match: 68.42%  ██████████████████████
      Skills needed: python, machine learning, sql, statistics, data analysis...
================================================
```

### Algorithm Explanation

#### Step 1: TF-IDF Vectorization
- **TF (Term Frequency)**: How often a skill appears in a job role
- **IDF (Inverse Document Frequency)**: How rare/unique the skill is across all roles
- **TF-IDF Score**: TF × IDF → Higher score = more discriminative skill

#### Step 2: Cosine Similarity
- Converts skill vectors into angle-based similarity (0 to 1)
- Formula: `cos(θ) = (A·B) / (||A|| × ||B||)`
- 1.0 = perfect match, 0.0 = no match

#### Step 3: Ranking
- Scores all 15 job roles
- Sorts by similarity (descending)
- Returns top N recommendations

---

