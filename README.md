# Contract-Based LLM Development Workflow

## Phase 1: Project Initialization 🎯

### Step 1: High-Level Project Spec Generation
Use a high-capability LLM (like Claude) with this prompt template:

```markdown
Please help me create a detailed project specification for the following project:

Project Description:
[Your prose description]

Generate:
1. Project Overview
2. Technical Requirements
3. System Architecture
4. Core Features List
5. Non-functional Requirements
6. Integration Points
7. Success Criteria

Format the output as a structured markdown document with clear sections and subsections.
```

### Step 2: Feature Breakdown
Use the same LLM to break down features:

```markdown
Based on this project specification:
[Paste project spec]

Please break this down into individual feature contracts. For each feature:
1. Input/Output Contracts
2. Dependencies
3. Integration Points
4. Success Criteria
5. Validation Steps

Format each feature as a separate markdown document.
```

## Phase 2: Feature Implementation Loop 🔄

### Step 1: Contract Generation
For each feature, use this prompt:

```markdown
Create a detailed technical contract for this feature:
[Paste feature description]

Generate:
1. Interface Definition
   - Input parameters
   - Output format
   - Error states
2. Validation Rules
   - Input constraints
   - Business rules
   - Edge cases
3. Test Scenarios
   - Happy path
   - Error cases
   - Edge cases
```

### Step 2: Implementation Workflow

#### A. Initial Implementation (IDE-integrated LLM)
```markdown
Implement the following contract:
[Paste contract]

Requirements:
1. Follow the exact interface specification
2. Implement input validation first
3. Add error handling as specified
4. Include inline documentation
5. Add type hints/annotations

Current codebase context:
[Relevant code snippets]
```

#### B. Validation Loop
For each implementation:

1. **Contract Compliance Check**
```markdown
Verify this implementation against the contract:
[Paste implementation]

Contract:
[Paste contract]

Check:
1. Interface compliance
2. Input validation
3. Error handling
4. Type safety
```

2. **Iteration Prompt (if needed)**
```markdown
The implementation violates these contract points:
[List violations]

Please modify only the affected components while maintaining:
1. Existing working functionality
2. Interface compliance
3. Error handling patterns
```

## Phase 3: Integration 🔗

### Step 1: Integration Contract
```markdown
Create an integration contract for:
Feature: [Feature name]
Existing Systems: [List systems]

Generate:
1. Integration points
2. Data flow
3. Error handling
4. Rollback procedures
```

### Step 2: Integration Implementation
```markdown
Implement the integration according to this contract:
[Paste integration contract]

Existing integration points:
[Paste relevant code]

Requirements:
1. Maintain existing interfaces
2. Add error handling
3. Include rollback logic
```

## Workflow Management Template 📋

### 1. Project Documentation Structure
```markdown
project/
├── specs/
│   ├── project_spec.md
│   └── features/
│       ├── feature1_contract.md
│       ├── feature2_contract.md
│       └── ...
├── implementations/
│   ├── feature1/
│   │   ├── contract.md
│   │   ├── implementation.md
│   │   └── validation.md
│   └── ...
└── integration/
    ├── contracts/
    └── implementations/
```

### 2. LLM Usage Guidelines

1. **Project-Level Planning (Claude/GPT-4)**
   - Project specification
   - Feature breakdown
   - Contract generation

2. **Implementation (IDE LLM)**
   - Code generation
   - Basic modifications
   - Simple fixes

3. **Contract Validation (Claude/GPT-4)**
   - Complex analysis
   - Architecture decisions
   - Integration planning

### 3. Context Management

1. **Essential Context per Prompt**
```markdown
ALWAYS INCLUDE:
1. Current contract
2. Immediate dependencies
3. Relevant error states

ROTATE AS NEEDED:
1. Implementation details
2. Test cases
3. Integration points
```

2. **Context Rotation Strategy**
- Keep contracts in separate files
- Reference by link/name
- Include only relevant sections

## Example Workflow

1. **Start with prose requirement:**
   ```
   "We need a user authentication system with JWT"
   ```

2. **Generate project spec** (Using Claude):
   ```markdown
   Please create a project specification for:
   [Paste requirement]
   ```

3. **Generate feature contracts** (Using Claude):
   ```markdown
   Based on this project spec:
   [Paste spec]
   Generate individual feature contracts
   ```

4. **Implementation loop** (IDE LLM):
   ```markdown
   Contract: [Paste current feature contract]
   Task: Implement the login endpoint
   Context: Express.js API
   ```

5. **Validation** (Claude):
   ```markdown
   Verify this implementation:
   [Paste code]
   Against this contract:
   [Paste contract]
   ```

## Key Success Factors 🎯

1. **Contract Clarity**
   - Explicit interfaces
   - Clear validation rules
   - Defined error states

2. **Context Management**
   - Rotate context efficiently
   - Keep contracts separate
   - Reference only needed parts

3. **LLM Selection**
   - Use powerful LLMs for planning
   - Use IDE LLMs for implementation
   - Use powerful LLMs for validation

4. **Documentation Structure**
   - Maintain clear hierarchy
   - Keep contracts accessible
   - Track validations

Would you like me to elaborate on any specific part or provide more detailed examples?
