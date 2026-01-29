# EdEHR Compass - Style Consistency & Content Gaps Report

**Report Generated:** 2026-01-28
**Audit Scope:** All markdown files in compass repository (user-guides, educational-implementation, getting-started, resources-and-casestudies, community)

---

## Executive Summary

This comprehensive audit reveals a well-structured documentation repository with strong consistency in heading hierarchy, list formatting, and procedural blocks. However, **critical accessibility gaps exist** in image captions and alt text across 23+ files, and **broken links** need immediate attention in primary navigation.

### Critical Findings:
- ❌ **23+ files** missing image captions and alt text (WCAG compliance issue)
- ❌ **4 broken links** in main README.md navigation table
- ❌ **Several incomplete guide sections** with placeholder content
- ⚠️ **Inconsistent callout syntax** mixing GitBook and Markdown styles
- ⚠️ **Mixed image hosting** between relative paths and external URLs

### Overall Grade: **B+ (Good structure, needs accessibility and completion work)**

---

## Part 1: Style Consistency Analysis

### 1.1 Heading Level Hierarchy

**Status: MOSTLY CONSISTENT ✅**

**Current Pattern:**
- H1 (#): Page titles (one per page) ✅
- H2 (##): Major section divisions ✅
- H3 (###): Subsections and content areas ✅
- H4 (####): Sub-subsections (inconsistent usage) ⚠️

**Issues Identified:**
1. Some files jump from H1 to H3 without H2 intermediary
2. H4 usage inconsistent - sometimes within `{% stepper %}` blocks, sometimes standalone
3. Files needing review:
   - `/user-guides/student-guides/navigating-the-student-dashboard.md`
   - `/educational-implementation/simtech-support-guide/.../role-overview-and-responsibilites.md`

**Recommendations:**
- Establish rule: H1 → H2 → H3 progression only
- Reserve H4 exclusively for stepper step titles
- Add H2 sections where files jump from H1 to H3

---

### 1.2 List Formatting

**Status: HIGHLY CONSISTENT ✅✅**

**Pattern Analysis:**
- **Bullet lists (*)**: Consistently used for unordered items
- **Numbered lists (1., 2., 3.)**: Consistently used for sequential steps
- **Spacing**: Single space after list marker (standardized)
- **No mixing** of `-` and `*` for bullets found

**Verdict:** No changes needed. Current implementation is excellent.

---

### 1.3 Image and Figure Conventions

**Status: HIGHLY INCONSISTENT ❌ (CRITICAL)**

**Critical Gap Identified:**

The vast majority of images have **empty captions** and **empty alt text**, representing a significant **WCAG 2.1 Level A compliance failure**.

**Current Implementation:**
```markdown
<figure><img src="path/to/image.png" alt=""><figcaption></figcaption></figure>
```

**Files Affected (23+ identified):**
- `/user-guides/managing-activities.md`
- `/user-guides/instructor-dashboard.md`
- `/user-guides/evaluating-student-work.md`
- `/user-guides/skills-assessment-mode.md`
- `/user-guides/course-designer/creating-your-first-edehr-activity.md`
- `/user-guides/course-designer/working-with-learning-objectives/README.md`
- `/user-guides/course-designer/working-with-learning-objectives/creating-learning-objectives.md`
- `/user-guides/course-designer/working-with-learning-objectives/editing-learning-objectives.md`
- `/user-guides/course-designer/working-with-learning-objectives/managing-learning-objectives.md`
- `/user-guides/course-designer/working-with-case-studies/README.md`
- `/user-guides/student-guides/students-getting-started/patient-search-and-selection.md`
- `/user-guides/student-guides/navigating-the-edehr-interface.md`
- And 12+ more files

**Additional Issues:**
1. **Mixed image hosting formats:**
   - Relative paths: `.gitbook/assets/`
   - External: `colony-recorder.s3.amazonaws.com`
   - CDN: `ajeuwbhvhr.cloudimg.io`

2. **Empty alt attributes:** Nearly all images have `alt=""`

**Recommendations (Priority 1 - CRITICAL):**
1. **Add descriptive captions** to all `<figcaption>` elements
2. **Populate alt text** with meaningful descriptions for screen readers
3. **Standardize image hosting** - choose relative paths or external URLs consistently
4. **Create caption template:**
   ```markdown
   <figure><img src=".gitbook/assets/example.png" alt="Screenshot showing the Submit button in the Learning Activity banner"><figcaption>Figure 1: Submitting your activity from the Learning Activity banner</figcaption></figure>
   ```

---

### 1.4 Code Block Usage

**Status: CONSISTENT BY DEFAULT ✅**

**Analysis:**
- Minimal code blocks in repository (appropriate for EHR user documentation)
- Inline code formatting (backticks) used consistently for UI elements
- No ` ``` ` code blocks found, avoiding inconsistency issues

**Verdict:** No changes needed. Documentation focuses on UI navigation rather than code.

---

### 1.5 Link Formatting

**Status: MOSTLY CONSISTENT ⚠️**

**Current Patterns:**
1. **Internal links (relative paths):**
   - Format: `[Link text](path/to/file.md)` ✅
   - Example: `[EdEHR vs other EHR Systems](../overview/edehr-vs-other-ehr-systems.md)` ✅

2. **External links:**
   - Format: `[Text](https://full-url)` ✅
   - Used for external resources and Gitbook app links

3. **Anchor links:**
   - Format: `[Text](file.md#section-heading)` ✅
   - Lowercase with hyphens

**Issues Identified:**
1. **Broken links in README.md** (see Content Gaps section)
2. **Inconsistent URL handling** - some files use full Gitbook app URLs instead of relative paths
3. **Mixed approaches** within same directory

**Recommendations:**
1. Prefer relative paths for all internal links
2. Use full URLs only for external resources
3. Document link naming convention in style guide

---

### 1.6 Callout/Hint Box Styles

**Status: MOSTLY CONSISTENT ⚠️**

**Current Implementation:**

**GitBook Syntax (Primary):**
```markdown
{% hint style="info" %}
Content here
{% endhint %}
```

**Style Types in Use:**
- `{% hint style="info" %}` - Information/tips
- `{% hint style="success" %}` - Positive notes
- `{% hint style="warning" %}` - Important cautions
- `{% hint style="danger" %}` - Critical warnings

**Stepper Blocks (Highly Consistent):**
```markdown
{% stepper %}
{% step %}
### Step Title
Content
{% endstep %}
{% endstepper %}
```

**Issue Identified:**

**Mixed callout formats found in:**
- `/user-guides/student-guides/students-getting-started/clinical-tasks-cheat-sheets.md`

Uses non-standard markdown blockquote format:
```markdown
> [!TIP]
> Content here
```

This is GitHub/Markdown syntax, not GitBook standard.

**Recommendations:**
1. **Convert all blockquote callouts** to GitBook `{% hint %}` syntax
2. **File to update:** `clinical-tasks-cheat-sheets.md` (2 instances)
3. **Establish hint style guide:**
   - `info`: General information, helpful notes, tips
   - `success`: Confirmations, successful outcomes, examples
   - `warning`: Important cautions, considerations before acting
   - `danger`: Critical warnings, irreversible actions

---

## Part 2: Content Gaps Analysis

### 2.1 Broken Links

**Status: CRITICAL GAPS IDENTIFIED ❌**

**Location: `/user-guides/README.md` (lines 13-14)**

**Broken Links in Role Navigation Table:**
1. **Faculty/Instructors:** `/broken/pages/TB8HEPlHk0HnR8Nj5ZEb`
2. **Students:** `/broken/pages/8vhOjbL46CaClgZS1hi5`
3. **Course Designers:** `/broken/pages/DgOrIbUkNnCv5p3Spvz7`
4. **Demo Users:** `/broken/pages/akFCrvBOgfhICbzp07ym`
5. **LMS Administrators:** Empty cell (no link)

**Impact:** High - This is the main navigation table in the User Guides landing page.

**Recommended Fixes:**
```markdown
Faculty/Instructors → [instructor-guides/accessing-instructor-functions.md]
Students → [student-guides/students-getting-started/README.md]
Course Designers → [course-designer/course-designer-guide.md]
Demo Users → [demonstration-mode/demonstration-mode.md]
LMS Administrators → [lms-admin/setting-up-edehr-in-your-lms.md]
```

---

### 2.2 Missing Content / Incomplete Guides

**Files with Placeholder or Incomplete Content:**

1. **`/user-guides/student-guides/navigating-the-student-dashboard.md`**
   - Listed in SUMMARY.md but content appears incomplete/minimal

2. **`/user-guides/student-guides/navigating-the-edehr-interface.md` (line 36)**
   - Contains: "User Settings (Placeholder for future features)"
   - Should note this is coming soon or remove reference

3. **`/user-guides/README.md` (lines 23, 37-41, 49-53)**
   - Missing guide pages referenced in overview:
     - "Providing Feedback" (Faculty section)
     - "Accessing Your Assignments" (Student section)
     - "Navigating the EHR Interface" (Student section)
     - "Documenting Patient Information" (Student section)
     - "Submitting Completed Work" (Student section)
     - "Reviewing Instructor Feedback" (Student section)
     - "Case Builder Tutorial" (Course Designer section)
     - "Creating Effective Assignments" (Course Designer section)
     - "Building Evaluation Rubrics" (Course Designer section)
     - "Mapping to Learning Objectives" (Course Designer section)
     - "Sharing and Importing Cases" (Course Designer section)

4. **`/user-guides/demonstration-mode/demonstration-mode.md`**
   - May need expansion based on broken link reference

5. **`/resources-and-casestudies/frequently-asked-questions.md`**
   - Should be verified for completeness

**Recommendation:**
- Either create these missing guide pages OR
- Remove references from README.md overview sections

---

### 2.3 Missing Screenshots/Images

**Content References to Images:**

Based on comment patterns in files, several screenshots are noted as needed but may not exist:

1. **`/user-guides/student-guides/scanning-medications-in-edehr.md`**
   - Lines 11, 21, 29, 37, 50, 59: "_Screenshot : Show..._" comments
   - May indicate placeholder text for images to be added

**Note:** Most image references appear to be present, but alt text and captions are missing (see Section 1.3).

---

### 2.4 Gaps in Role-Based Coverage

**Analysis of Documentation Coverage by Role:**

| Role | Coverage Level | Gaps Identified |
|------|----------------|-----------------|
| **Students** | GOOD | Missing: Accessing assignments guide, Reviewing feedback details |
| **Instructors** | EXCELLENT | Complete guides for evaluation, activities, class lists |
| **Course Designers** | EXCELLENT | Complete guides for Learning Objects and Case Studies |
| **LMS Admins** | MODERATE | Single guide present, could expand troubleshooting |
| **Demo Users** | MINIMAL | Single page, may need expansion for evaluation purposes |
| **Simulation Techs** | GOOD | Comprehensive support guide in educational-implementation |

**Recommendations:**
1. **Expand Student guides:** Add missing sections noted in 2.2
2. **Expand Demo User documentation:** Add evaluation checklist, feature comparison
3. **Add LMS Admin troubleshooting:** Common issues and solutions section

---

### 2.5 Section References to Non-Existent Content

**Found References:**

1. **`/user-guides/README.md`**
   - "→ Faculty Implementation Strategies" (referenced but no link)
   - "→ Student Success Resources" (referenced but no link)
   - "→ Instructional Design Strategies" (referenced but no link)
   - These appear to be planned sections

2. **Cross-references in guides:**
   - Most internal cross-references appear valid
   - Links use relative paths correctly

**Recommendation:** Either create these "Strategy" sections or remove the arrow references.

---

## Part 3: Recommendations Summary

### Priority 1: CRITICAL (Implement Immediately)

1. **Add image captions and alt text** (23+ files)
   - Accessibility compliance issue (WCAG 2.1 Level A)
   - Improves usability for all users
   - Estimated effort: 3-5 hours

2. **Fix broken links in README.md** (5 links)
   - Main navigation table is broken
   - High user impact
   - Estimated effort: 15 minutes

### Priority 2: HIGH (Implement Soon)

3. **Complete or remove missing guide references** (15+ pages)
   - User expectations vs. actual content mismatch
   - Affects user trust
   - Estimated effort: Decision required, then 10-20 hours if creating content

4. **Standardize callout syntax** (1-2 files)
   - Convert markdown blockquotes to GitBook hints
   - File: clinical-tasks-cheat-sheets.md
   - Estimated effort: 10 minutes

### Priority 3: MEDIUM (Plan for Future Iteration)

5. **Standardize image hosting approach**
   - Choose relative paths OR external URLs consistently
   - Document decision in style guide
   - Estimated effort: 2-3 hours + migration time

6. **Expand role-based coverage**
   - Add Student assignment access guide
   - Expand Demo User documentation
   - Add LMS Admin troubleshooting
   - Estimated effort: 5-8 hours

### Priority 4: LOW (Nice to Have)

7. **Refine heading hierarchy edge cases**
   - Fix H1 → H3 jumps in 2-3 files
   - Document H4 usage policy
   - Estimated effort: 1 hour

8. **Create comprehensive style guide**
   - Document all standards from this audit
   - Share with contributors
   - Estimated effort: 2 hours

---

## Part 4: Style Guide Recommendations

### Proposed Style Standards

**To ensure future consistency, establish these standards:**

#### Headings
- One H1 per page (page title only)
- Use H2 for major sections
- Use H3 for subsections
- Reserve H4 for stepper step titles only
- Never skip heading levels

#### Lists
- Use `*` for unordered lists
- Use `1. 2. 3.` for sequential steps
- Single space after marker
- Consistent indentation (2 spaces per level)

#### Images
```markdown
<figure>
  <img src=".gitbook/assets/filename.png" alt="Descriptive text for screen readers">
  <figcaption>Figure X: Brief description of what the image shows</figcaption>
</figure>
```

#### Links
- Internal: `[Text](relative/path/to/file.md)`
- External: `[Text](https://full-url.com)`
- Anchors: `[Text](file.md#lowercase-with-hyphens)`

#### Callouts
```markdown
{% hint style="info" %}
General information and tips
{% endhint %}

{% hint style="success" %}
Positive confirmations and examples
{% endhint %}

{% hint style="warning" %}
Important cautions and considerations
{% endhint %}

{% hint style="danger" %}
Critical warnings about irreversible actions
{% endhint %}
```

#### Procedural Steps
```markdown
{% stepper %}
{% step %}
#### Step Title
Content and instructions
{% endstep %}
{% endstepper %}
```

---

## Part 5: Files Requiring Immediate Attention

### Image Caption Issues (23+ files):
1. `/user-guides/managing-activities.md`
2. `/user-guides/instructor-dashboard.md`
3. `/user-guides/evaluating-student-work.md`
4. `/user-guides/skills-assessment-mode.md`
5. `/user-guides/course-designer/creating-your-first-edehr-activity.md`
6. `/user-guides/course-designer/working-with-learning-objectives/README.md`
7. `/user-guides/course-designer/working-with-learning-objectives/creating-learning-objectives.md`
8. `/user-guides/course-designer/working-with-learning-objectives/editing-learning-objectives.md`
9. `/user-guides/course-designer/working-with-learning-objectives/managing-learning-objectives.md`
10. `/user-guides/course-designer/working-with-case-studies/README.md`
11. `/user-guides/student-guides/students-getting-started/patient-search-and-selection.md`
12. `/user-guides/student-guides/navigating-the-edehr-interface.md`
13. `/user-guides/student-guides/submitting-work-and-feedback/submitting-work-and-closing-the-chart.md`
14. `/user-guides/instructor-guides/accessing-instructor-functions.md`
15. `/user-guides/managing-class-lists.md`
16. `/user-guides/instructor-tools-and-navigation.md`
17. Plus 7+ additional files in working-with-case-studies and educational-implementation

### Broken Links:
- `/user-guides/README.md` (role navigation table - 5 links)

### Callout Format Issues:
- `/user-guides/student-guides/students-getting-started/clinical-tasks-cheat-sheets.md` (2 instances)

### Incomplete Content:
- `/user-guides/student-guides/navigating-the-student-dashboard.md`
- `/user-guides/README.md` (15+ missing guide references)
- `/user-guides/demonstration-mode/demonstration-mode.md`

---

## Part 6: Positive Findings

**Strengths of Current Documentation:**

1. ✅ **Excellent heading hierarchy** across most files
2. ✅ **Highly consistent list formatting** (no variations)
3. ✅ **Well-implemented stepper blocks** for procedural content
4. ✅ **Good use of frontmatter** with icons and descriptions
5. ✅ **Strong internal link structure** (aside from identified broken links)
6. ✅ **Comprehensive coverage** of instructor and course designer roles
7. ✅ **Clear navigation structure** in SUMMARY.md files
8. ✅ **Good use of GitBook features** (hints, steppers, columns)
9. ✅ **Consistent file naming** (kebab-case)
10. ✅ **Well-organized directory structure** by role

---

## Conclusion

The EdEHR Compass documentation demonstrates strong structural consistency and thoughtful organization. The primary gaps are in **accessibility compliance** (image captions/alt text) and **content completeness** (broken links and missing guides).

**Recommended Action Plan:**
1. **Week 1:** Fix broken links + add image captions/alt text (Priority 1)
2. **Week 2-3:** Complete or remove missing guide references (Priority 2)
3. **Week 4:** Standardize callouts and image hosting (Priority 2-3)
4. **Future:** Expand role-based coverage and create style guide (Priority 3-4)

**Estimated Total Effort:** 15-30 hours depending on scope of content creation decisions.

---

**Report compiled by:** Claude (EdEHR Compass Documentation Audit)
**For questions or clarifications, contact the EdEHR documentation team.**
