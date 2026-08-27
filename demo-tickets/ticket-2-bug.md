Host note: clean bug report, includes a stack trace to show the model
ignoring irrelevant technical noise. Expected category: bug.

---

Subject: App crashes when exporting a report larger than 10k rows

Every time I try to export our monthly usage report (currently
around 14,000 rows) to CSV, the app freezes for a few seconds and
then shows a white screen. The browser console has this:

Uncaught RangeError: Invalid array length
    at ReportExporter.buildRows (report-exporter.js:412)
    at ReportExporter.export (report-exporter.js:88)
    at onClick (ExportButton.tsx:23)

Exports under ~5,000 rows work fine. This started happening after
last week's update. Using Chrome 128 on Windows 11. This is blocking
our end-of-month reporting, please help.
