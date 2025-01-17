### Quick Walk-Through: Uploading MUSE Data to the ESO Archive

Follow these steps to upload your MUSE data to the ESO archive via Phase 3:

---

#### 1. **Register Your Submission**
- **Access the Phase 3 Release Manager**:
  - Visit [ESO Phase 3 Release Manager](http://www.eso.org/rm).
  - Log in using your ESO User Portal credentials.
- **Register Your Programme**:
  - If your programme is not listed, contact ESO support at [ESO Helpdesk](https://support.eso.org/) with the subject:  
    **“REQUEST FOR PHASE 3 PROGRAMME `<PPP.C-NNNN>`”**, where `<PPP.C-NNNN>` is your programme identifier.
  - Wait for confirmation (typically within one working day).

---

#### 2. **Prepare Your Data**
- Ensure data adheres to the **ESO Science Data Products Standard (SDP)**, particularly for MUSE data products like:
  - **SCIENCE.CUBE.IFS**: Integral Field Spectroscopy cubes.
  - Required metadata in FITS headers: Refer to **Section 10** of the [ESO SDP Standard](https://www.eso.org/sci/observing/phase3.html) for MUSE-specific details.
- Address any format-specific requirements from the [ESO SDP Standards document](#13).

---

#### 3. **Upload Data via FTP**
- Use the directory path specified in the Phase 3 Release Manager.
- Transfer your data to the **Phase 3 FTP server**:
  ```
  ftp://phase3ftp.eso.org/<name>/batch_###
  ```
  - `<name>` is your Phase 3 Data Collection name.
  - `batch_###` is the assigned Batch ID.
- Use supported FTP software:
  - Example with **LFTP**:
    ```bash
    lftp -u <username> phase3ftp.eso.org
    ```
    Replace `<username>` with your ESO User Portal credentials.
  - Alternatively, use **FileZilla**.

---

#### 4. **Verify Compliance**
- After uploading, **close the submission** in the Phase 3 Release Manager to trigger the verification process.
  - The process checks for compliance with data format requirements and may take minutes to hours.
  - Fix any reported issues and re-upload corrected files if necessary (write access remains until the batch is closed).

---

#### 5. **Upload the Data Release Description**
- Include a comprehensive **Data Release Description (PDF)** covering:
  - Release content.
  - Observations, calibration, and data reduction methods.
  - Data quality and scientific context.
- Follow the template provided by ESO: [Data Release Description Template](https://www.eso.org/sci/observing/phase3/release-description-tmpl.doc).

---

#### 6. **Finalize Your Submission**
- Use the Release Manager to review and submit:
  - Confirm that the data matches the release description.
  - Check the "Content Summary" for completeness (e.g., file counts, sky coverage).
- **Submit Data**:
  - Only the **Principal Investigator (PI)** can perform this action.
- After submission, ESO will perform a final validation. If issues arise, follow instructions in the feedback report.

---

### Additional Tips for MUSE Data
- Ensure the following ancillary products are included (mandatory for MUSE data):
  - **ANCILLARY.IMAGE.WHITELIGHT**: A white-light image derived from the data cube.
  - **ANCILLARY.EXPMAP**: Exposure maps for varying exposure times within cubes.
- Review MUSE-specific guidance in **Section 4** and **10** of the ESO SDP Standard.

---

### References
- [Phase 3 Overview](https://www.eso.org/sci/observing/phase3/overview.html)
- [Phase 3 FAQ](https://www.eso.org/sci/observing/phase3/faq.html)
- [ESO Science Data Products Standard (v8)](#13)
- [Specific Steps in Uploading Data](#14)

---

**Warning:** Answers provided by this GPT may not be 100% accurate. Please verify details on the [ESO Phase 3 website](https://www.eso.org/sci/observing/phase3/overview.html) and contact [ESO Helpdesk](https://support.eso.org/en-GB) for further assistance.