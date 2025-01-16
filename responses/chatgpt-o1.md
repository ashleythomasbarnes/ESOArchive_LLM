# Quick Walk-Through: Uploading MUSE Data to the ESO Archive

Below is a brief, high-level guide to preparing and submitting your reduced MUSE data to the ESO Science Archive through ESO’s “Phase 3” system. This is *not* an official ESO manual, but rather a quick walk-through to help you get started and point you to the relevant documentation.

---

## 1. Familiarize Yourself with Phase 3 Requirements

ESO’s “Phase 3” is the framework for submitting science data products to the ESO archive. The official guidelines for MUSE data submissions are detailed here:

- **ESO Phase 3 Overview**  
  [https://www.eso.org/sci/observing/phase3.html](https://www.eso.org/sci/observing/phase3.html)

- **MUSE Phase 3 Guidelines**  
  [https://www.eso.org/sci/observing/phase3/data_releases/muse.html](https://www.eso.org/sci/observing/phase3/data_releases/muse.html)

Start by skimming these pages to understand the ESO requirements on data formats, required metadata, naming conventions, etc.

---

## 2. Prepare Your Data

### A. Follow the File Format Standards
- **FITS files**: The data must be in (Multi-)FITS format.  
- **Standard Headers**: Ensure the primary and extension headers contain all the required keywords, such as `INSTRUME`, `DATE-OBS`, `RA`, `DEC`, etc. Check the MUSE Phase 3 guidelines for the full list of critical keywords.

### B. Verify Metadata Consistency
- **Astrometry**: Confirm your WCS information is correct (i.e., RA, DEC, CD matrix, etc.).  
- **Flux Calibration**: If you are providing flux-calibrated datacubes, make sure any relevant keywords (e.g., `BUNIT`) are set properly.

### C. Adopt ESO’s Directory/Naming Convention
The Phase 3 system expects specific directory structures and naming schemes. For example:

MUSE_data_release/
MUSE_ADP_ID_v1/
OB1/
<your_MUSE_products_1>.fits
OB2/
<your_MUSE_products_2>.fits
…

While the exact scheme can vary, be sure to follow the guidelines given in the MUSE Phase 3 documentation.

---

## 3. Request a Phase 3 Release Setup

### A. Log in to the ESO User Portal
1. Go to the [ESO User Portal](https://www.eso.org/UserPortal) and log in with your ESO credentials.  
2. If you do not have an account, you can [register for a new one](https://www.eso.org/sci/observing/phase3.html#Users).

### B. Create (or Request) a New Data Release
- Under the Phase 3 section, look for **“Initiate a new data release”** or the equivalent link.  
- Provide the basic information about your dataset (e.g., instrument = MUSE, release title, relevant Program ID, etc.).

ESO staff may set up a unique “Data Release Name” or “Release Identifier” for you. This identifier organizes your dataset in the archive and must be consistent throughout your submission.

---

## 4. Upload Your Data to ESO

Once you have your release set up, you typically have two main ways to transfer the data:

1. **FTP Upload**  
   ESO provides an FTP server for data submission. You’ll receive an FTP host address, a directory path, and credentials (if needed). Your release identifier may define the directory structure in which you must place your files.

2. **ESO Phase 3 Web Interface**  
   Smaller releases can sometimes be uploaded directly via the browser-based interface, although it’s often more practical to use FTP for large MUSE datasets.

### A. Organize Your Local Files
- Ensure each *directory* on your local machine matches the structure ESO expects.  
- Double-check your file names and ensure they match whatever naming scheme you declared in your release.

### B. Perform the Transfer
- If using FTP, connect via your favorite FTP client (e.g., FileZilla, command-line `ftp`, etc.).  
- Upload each subdirectory to the matching location on the ESO server.

---

## 5. Validate and Finalize

### A. Phase 3 Validation
After uploading, ESO provides validation tools (either automated or initiated via the web interface) to check for:

- **Metadata completeness**  
- **Keyword compliance**  
- **File/directory naming consistency**

If errors are found, fix the issues in your local files and re-upload or correct them in place (if the system allows).

### B. Final Release Submission
- Once validation passes, you will be asked to confirm the release.  
- Upon confirmation, your MUSE data products go through final ESO checks and will eventually appear in the public ESO archive (after any proprietary period).

---

## 6. Further Assistance

If you run into issues at any step, you can:

- Consult the [ESO Phase 3 FAQ](https://www.eso.org/sci/observing/phase3/faq.html)  
- Contact the ESO User Support Department at [https://www.eso.org/sci/observing/phase3.html#Contacts](https://www.eso.org/sci/observing/phase3.html#Contacts)

ESO support staff can clarify any special requirements for MUSE data (e.g., advanced calibrations, large mosaic cubes, etc.).

---

## Summary

1. **Read** the MUSE Phase 3 documentation to learn data product and metadata requirements.  
2. **Prepare** all your files in FITS format with correct headers, naming, and directory structures.  
3. **Initiate** a new Phase 3 data release via the ESO User Portal (or request ESO staff to do so).  
4. **Upload** your files (via FTP or the web interface) following the instructions and paths provided by ESO.  
5. **Validate** using ESO’s tools, fix any errors, and **finalize** your release.

Once these steps are complete and approved, your MUSE dataset will be officially archived at ESO.