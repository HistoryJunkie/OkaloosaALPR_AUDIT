### Phase 1: Preparation (The "Local" Clean)

Before you look at a map, you must define what "correct" looks like.

1. **Define your Schema:** Decide on the exact tags you will use (e.g., `man_made=surveillance`, `surveillance:type=ALPR`, `manufacturer=Flock Safety`).
2. **Run a Discovery Query:** Use your database to find every record that contains "Flock" or "ALPR" in *any* tag field.
3. **Flag for Review:** Add a column in your database called `audit_status`. Mark these discovered records as `needs_review`.

---

### Phase 2: Batching (The "County-by-County" Approach)

Trying to audit 97k points at once is where the pain comes from.
4.  **Export a "Small Batch":** Filter your database by a single county (e.g., Okaloosa).
5.  **Generate a GeoJSON:** Save only that county's `needs_review` records into a single file.
6.  **Open JOSM:** Download the live OSM data for that specific county.

---

### Phase 3: The JOSM Power Move (The "Smooth" Part)

This is where the actual work happens. You are not clicking points; you are managing a list.
7.  **Import your GeoJSON:** Layer your database points over the live OSM data in JOSM.
8.  **Use the "Todo List" Plugin:** Add all imported points to the Todo list.
9.  **The "Next" Workflow:** Click "Next" in the plugin. JOSM will automatically zoom to the first camera.
10. **Apply Presets:** Select the camera, apply your "Correct Schema" (you can save this as a button/preset), and move to the next.

---

### Phase 4: Validation & Upload

OSM requires a high standard for bulk edits to avoid "vandalism" flags.
11. **Run the Validator:** Use JOSM’s built-in validation tool to check for common errors (like overlapping nodes).
12. **Craft a Changeset Comment:** Write a clear description of your work (e.g., *"Auditing ALPR manufacturer tags in Okaloosa County based on public records."*).
13. **Upload:** Send the batch to OSM.
14. **Update Local Database:** Mark those specific IDs in your database as `uploaded`.

---

### Phase 5: Repeat

15. **Move to the next county.**

### Why this is the "Pro" way:

* **Safety:** You aren't "guessing" with a Python script; you are visually confirming each camera in JOSM.
* **Traceability:** By keeping an `audit_status` in your DB, you never lose track of what is finished.
* **Community Trust:** Batching by county with clear comments makes you a "good citizen" in the eyes of OSM moderators.
