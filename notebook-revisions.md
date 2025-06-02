# Notebook Revisions

## Project Overview
This file tracks notes and revisions for jupyter notebooks and code in the 'Understanding Animals' repository. These notes are used to track changes that need to be made for the Wild Winnipeg OER project.

**Status Legend:** ✅ Complete | 🔄 In Progress | ❌ Not Started | ⚠️ Blocked

---

## High-Level Project Tasks

### Data Infrastructure 🔄
- [ ] **LOW** - Migrate from Google Drive to Borealis API for data access
- [ ] **LOW** - Test Borealis Python API functionality  
- [ ] **HIGH** - Update all data access code across notebooks - using google drive

### Documentation & Integration 🔄
- [ ] **LOW** - Verify each notebook is linked in OER
- [ ] **LOW** - Add pressbook links to all notebook introductions
- [ ] **MEDIUM** - Create notebook appendix for OER
- [ ] **MEDIUM** - Add/update 'Run in Colab' labels

### Testing & Quality Assurance 🔄
- [ ] **HIGH** - Test all notebooks in Google Colab
- [ ] **HIGH** - Fix temporary data access (data should be in a single public google drive folder for testing)

---

## Notebook Categories & Status

### 📊 Object Detection & Classification
| Notebook | Status | Priority Issues | Est. Effort |
|----------|--------|----------------|-------------|
| `Completed_boundingboxcoco.ipynb` | ✅ | Data access, undefined variables --> Now fixed | 2-3 hours |
| `COMPLETED-ResNet50-bounding-boxes.ipynb` | ⚠️ | Has been simplified but not tested due to missing data | 4-5 hours | *Update: first chapter's input folder (4370-subset folder) is missing in our shared data in Google Drive. This is the input folder for most of the notebook's scripts.* 
| `COMPLETED-yolov5-pretrained.ipynb` | ✅ | No issues/errors | - |
| `Completed.All Datasizes.Classifier.ipynb` | ✅ | Has been split into 2 notebooks. | 6-8 hours | renamed to 100-500-1000-5000.Datasizes.Matrices.ipynb
| `Completed.Classification-Report.ipynb` | ✅ | Split from datasizes classifier notebook. | - | renamed to 100-500-1000-5000.Classification-Report.ipynb  *these 2 new notebooks need to be uploaded and the All.Datasizes.Classifier.ipynb needs to be deleted off github.*

### 🎨 Image Generation & Synthesis  
| Notebook | Status | Priority Issues | Est. Effort |
|----------|--------|----------------|-------------|
| `Stable Diffusion.ipynb` | ⚠️ | Removed some sections that were documentations and not code | 3-4 hours |
| `Blender.ipynb` | ⚠️ | No code, move to pressbook | 1 hour |
| `Prompt Generator.ipynb` | ✅ | Broken code blocks have been fixed, no more errors. | 2 hours | 

### 🔍 Dataset Exploration & Filtering
| Notebook | Status | Priority Issues | Est. Effort |
|----------|--------|----------------|-------------|
| `COMPLETED-image-filter.ipynb` | ✅ | Minor repetition cleanup | 1 hour |
| `COMPLETED-random-manual-review.ipynb` | ✅ | Ready | - |
| `COMPLETED-ft-data-prep.ipynb` | ✅ | No output errors. Still need to improve intro, add dataset options | 2 hours |

### 📈 Visualization & Analysis
| Notebook | Status | Priority Issues | Est. Effort |
|----------|--------|----------------|-------------|
| `COMPLETED-close-encounters.ipynb` | ✅.✅ | *One output error has been fixed, but test output pdf is blank(?)* | - |
| `COMPLETED-matplotlib-visualization.ipynb` | ✅ | No issues/errors| Jenelle |
| `COMPLETED-random-interactive-image.ipynb` | ✅ | Tested & cleaned the notebook | - |
| `COMPLETED-sightings-bar-graph.ipynb` | ✅.⚠️ | No issues/errors | Jenelle added intro, but vscode github setup is not proper, we need help|
| `COMPLETED-treemap.ipynb` | ✅.✅ | No issues/errors | - |
| `COMPLETED_100grid.ipynb` | ✅.✅ | No cell output errors, *but generated grid images need to be checked in its output folder* | - |

### 🔧 Miscellaneous Tools
| Notebook | Status | Priority Issues | Est. Effort |
|----------|--------|----------------|-------------|
| `Completed_Photoselect tool notebook.ipynb` | ⚠️ | Broken functions, optional for OER | 3 hours |

---

## Issue Categories

### 🔗 Data Access Issues
**Root Cause:** Google Drive credential propagation failures
- `Completed_boundingboxcoco.ipynb` - Data access method needs change
- `Completed.All Datasizes.Classifier.ipynb` - All Google Drive references need updating
- **Solution:** Implement Borealis API across all notebooks

### 🔧 Code Structure Issues
**Pattern:** Functions broken across multiple code blocks
- `Completed_Photoselect tool notebook.ipynb` - Functions segmented
- `Prompt Generator.ipynb` - Functions broken up
- `Completed.All Datasizes.Classifier.ipynb` - Duplicate functions, broken blocks
- **Solution:** Consolidate functions into single code blocks

### 📝 Documentation Issues
**Pattern:** Missing or unclear introductions
- All notebooks need pressbook links
- Several notebooks lack clear purpose statements
- `COMPLETED-ft-data-prep.ipynb` needs dataset comparison info
- **Solution:** Standardize introduction template

### ⚙️ Technical Issues
**Pattern:** CoLab compatibility and undefined variables
- `Completed_boundingboxcoco.ipynb` - 'image_path' variable undefined
- Several notebooks have untested CoLab compatibility
- **Solution:** Systematic CoLab testing protocol

---

## Detailed Notebook Issues

### High Priority Fixes

#### `Completed.All Datasizes.Classifier.ipynb` ❌
**Issues:**
- [ ] Unclear purpose/introduction
- [ ] Google Drive data access needs migration
- [ ] Appears to be merged from 2 notebooks (very long)
- [ ] `mount_google_drive()` function defined twice
- [ ] `safe_get_image_files()` function defined twice  
- [ ] `process_datasets` function defined but unused (typo for `process_dataset`?)
- [ ] Functions broken across code blocks
- [ ] Has pre-run cloud outputs (clarify these can't run in CoLab)

**Recommended Action:** Split into 2 focused notebooks

#### `COMPLETED-ResNet50-bounding-boxes.ipynb` 🔄
**Issues:**
- [ ] Contains 3 independent sections
- [ ] Should be split into 3 separate notebooks

**Recommended Action:** Create focused single-purpose notebooks

#### `Completed_boundingboxcoco.ipynb` ⚠️
**Issues:**
- [ ] Data access method needs change
- [ ] `image_path` variable not defined
- [ ] Removed reference to individual images (can restore from main branch if needed)

### Medium Priority Fixes

#### `Stable Diffusion.ipynb` ❌
**Issues:**
- [ ] Very large file size
- [ ] Consider splitting for better usability

#### `COMPLETED-ft-data-prep.ipynb` 🔄
**Issues:**
- [ ] Introduction needs dataset comparison (beyond COCO)
- [ ] Should explain dataset selection criteria

#### `COMPLETED-image-filter.ipynb` ✅
**Issues:**
- [ ] Somewhat repetitive sections
- [ ] Could add summary of changes needed per filter type

### Low Priority / Optional

#### `Completed_Photoselect tool notebook.ipynb` ⚠️
**Status:** Optional for final OER version
**Issues:**
- [ ] Functions broken into segments
- [ ] Very specific/ideosyncratic functionality
- [ ] Test in CoLab to determine if salvageable

#### `Blender.ipynb` ⚠️
**Status:** Move to pressbook as static content
**Issues:**
- [ ] Very large file
- [ ] Contains no executable code
- [ ] Documents AV's synthetic animal work

---

## Organization Recommendations

### Folder Structure
```
jupyter-notebooks/
├── 01-Dataset-Exploration/
├── 02-Object-Detection/  
├── 03-Classification/
├── 04-Visualization/
├── 05-Synthetic-Generation/
└── 99-Miscellaneous/
```

### Notebook Naming Convention
- Use consistent prefixes: `01-`, `02-`, etc.
- Include functionality in name
- Remove "COMPLETED" prefix after reorganization

---

## Testing Protocol

### CoLab Testing Checklist
- [ ] All code blocks run in sequence without errors
- [ ] Data sources accessible
- [ ] Outputs generate correctly
- [ ] Introduction/documentation accurate
- [ ] Links to pressbook functional

### Quality Standards
- Each notebook should have single, clear purpose
- All functions should be complete in single code blocks
- Introductions must explain purpose and usage
- Data access should work via Borealis API

---

## Completion Tracking

**Overall Progress:** 40% Complete

**Next Sprint Priorities:**
1. Fix data access infrastructure (Borealis API)
2. Split large notebooks (`Completed.All Datasizes.Classifier.ipynb`, `COMPLETED-ResNet50-bounding-boxes.ipynb`)
3. Test all notebooks in CoLab
4. Standardize introductions and documentation

**Estimated Total Effort:** 25-35 hours