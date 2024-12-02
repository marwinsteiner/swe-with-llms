# Project Initialization

## 1. Project Overview File (`project_overview.md`)

### Template Structure
```markdown
# Project Overview

## 1. Project Information
- Project Name
- Version
- Last Updated
- Status
- Team/Owner

## 2. Business Context
- Problem Statement
- Business Objectives
- Success Criteria
- Key Stakeholders

## 3. Project Scope
- Core Features
- Feature Priority Matrix
- Out of Scope Items
- Dependencies

## 4. Timeline & Milestones
- Project Phases
- Key Deliverables
- Critical Deadlines
- Release Schedule

## 5. Resources & Constraints
- Team Resources
- Technical Requirements
- Budget Constraints
- Time Constraints

## 6. Risk Assessment
- Technical Risks
- Business Risks
- Mitigation Strategies
- Contingency Plans

## 7. Success Metrics
- KPIs
- Performance Metrics
- Quality Metrics
- Acceptance Criteria
```

### Prompt to Generate Project Overview
```markdown
Please create a comprehensive project overview document following this structure:

Project Context:
[Your project description]

Generate a detailed project overview document that includes:
1. Project Information
2. Business Context
3. Project Scope
4. Timeline & Milestones
5. Resources & Constraints
6. Risk Assessment
7. Success Metrics

Requirements:
- Be specific and quantifiable where possible
- Include clear success criteria
- Define measurable KPIs
- List concrete deliverables
- Identify key stakeholders
- Outline major risks and mitigation strategies

Format the output as a structured markdown document following the template above.
```

## 2. Architecture File (`architecture.md`)

### Template Structure
```markdown
# System Architecture

## 1. System Overview
- Architecture Style
- Design Principles
- System Context
- Key Constraints

## 2. Component Architecture
- Core Components
- Component Relationships
- Interface Definitions
- Data Flow

## 3. Technical Stack
- Programming Languages
- Frameworks
- Libraries
- Tools & Services

## 4. Data Architecture
- Data Models
- Storage Solutions
- Data Flow
- Data Security

## 5. Integration Architecture
- External Systems
- APIs
- Integration Points
- Authentication/Authorization

## 6. Deployment Architecture
- Infrastructure
- Deployment Strategy
- Scaling Approach
- Monitoring & Logging

## 7. Security Architecture
- Security Model
- Access Control
- Data Protection
- Security Protocols

## 8. Performance Architecture
- Performance Requirements
- Scalability Strategy
- Caching Strategy
- Load Handling

## 9. Development Architecture
- Development Environment
- Build Process
- Testing Strategy
- CI/CD Pipeline
```

### Prompt to Generate Architecture Document
```markdown
Please create a detailed system architecture document based on these requirements:

Project Context:
[Your project description]

Technical Requirements:
[Your technical requirements]

Generate a comprehensive architecture document that covers:
1. System Overview
2. Component Architecture
3. Technical Stack
4. Data Architecture
5. Integration Architecture
6. Deployment Architecture
7. Security Architecture
8. Performance Architecture
9. Development Architecture

Requirements:
- Focus on maintainability and scalability
- Include clear component relationships
- Define all integration points
- Specify security measures
- Detail performance considerations
- Outline development workflows

Format the output as a structured markdown document following the template above.
```

## 3. Usage Guidelines

1. **Initial Generation**
   - Use a powerful LLM (Claude/GPT-4) for initial document generation
   - Provide comprehensive project context
   - Review and refine generated content

2. **Document Maintenance**
   - Update documents when requirements change
   - Version control all documentation
   - Keep timestamps of last updates

3. **Integration with Development**
   - Reference documents in implementation tasks
   - Update based on technical discoveries
   - Maintain traceability to requirements

4. **Review Process**
   - Regular documentation reviews
   - Stakeholder sign-off
   - Change tracking
   - Version history

## 4. Best Practices

1. **Content**
   - Be specific and measurable
   - Use clear, concise language
   - Include diagrams where helpful
   - Maintain consistency across documents

2. **Structure**
   - Follow template hierarchy
   - Use consistent formatting
   - Include table of contents
   - Cross-reference related sections

3. **Maintenance**
   - Regular updates
   - Version control
   - Change logs
   - Review cycles

4. **Integration**
   - Link to related documents
   - Reference implementation details
   - Track dependencies
   - Maintain traceability

Would you like me to elaborate on any specific aspect of these documentation templates or provide more detailed examples?
