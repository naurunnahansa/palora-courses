# Palora Courses

Course content repository for the Palora learning platform.

## Structure

```
{exam-board}/
  {qualification}-{subject}/
    _course.json         # Course metadata
    content/
      {NN}-{unit-slug}/
        _unit.json       # Unit metadata
        {NN}-{topic}.json  # Topic content pages
```

## Folders

- **generic/** - Board-agnostic courses (common core content)
- **aqa/** - AQA (UK exam board)
- **cambridge/** - Cambridge Assessment International Education
- **edexcel/** - Pearson Edexcel (UK & International)

## Courses

### Generic (No Exam Board)
| Subject | Slug |
|---------|------|
| Physics | `generic/physics` |
| Chemistry | `generic/chemistry` |
| Biology | `generic/biology` |
| Mathematics | `generic/maths` |

### AQA GCSE
| Subject | Specification | Slug |
|---------|--------------|------|
| Physics | 8463 | `aqa/gcse-physics` |
| Chemistry | 8462 | `aqa/gcse-chemistry` |
| Biology | 8461 | `aqa/gcse-biology` |
| Mathematics | 8300 | `aqa/gcse-maths` |

### Cambridge IGCSE
| Subject | Syllabus | Slug |
|---------|----------|------|
| Physics | 0625 | `cambridge/igcse-physics` |
| Chemistry | 0620 | `cambridge/igcse-chemistry` |
| Biology | 0610 | `cambridge/igcse-biology` |
| Mathematics | 0580 | `cambridge/igcse-maths` |

### Edexcel GCSE
| Subject | Specification | Slug |
|---------|--------------|------|
| Physics | 1PH0 | `edexcel/gcse-physics` |
| Chemistry | 1CH0 | `edexcel/gcse-chemistry` |
| Biology | 1BI0 | `edexcel/gcse-biology` |
| Mathematics | 1MA1 | `edexcel/gcse-maths` |

### Edexcel IGCSE (International)
| Subject | Specification | Slug |
|---------|--------------|------|
| Physics | 4PH1 | `edexcel/igcse-physics` |
| Chemistry | 4CH1 | `edexcel/igcse-chemistry` |
| Biology | 4BI1 | `edexcel/igcse-biology` |
| Mathematics | 4MA1 | `edexcel/igcse-maths` |

## Content Schema

### _course.json
```json
{
  "slug": "aqa-gcse-physics",
  "title": "AQA GCSE Physics",
  "description": "Course description...",
  "examBoard": "AQA",
  "qualification": "GCSE",
  "specificationCode": "8463",
  "subject": "physics",
  "difficulty": "intermediate",
  "estimatedDuration": 50,
  "thumbnailUrl": "https://...",
  "isPublished": false,
  "isFree": false
}
```

### _unit.json
```json
{
  "title": "Forces",
  "description": "Newton's laws, motion, and momentum",
  "order": 1
}
```

### Topic content (e.g., 01-newtons-laws.json)
```json
{
  "title": "Newton's Laws of Motion",
  "content": "# Newton's Laws of Motion\n\n## First Law...",
  "order": 1
}
```
