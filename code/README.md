# Key findings from this run

Original and Augmented images come from two structurally different pipelines, not the same images at different stages. Every Augmented image is exactly 512×512 (0.0% deviate), while every Original image is at its native capture resolution (100% deviate from 512×512) — phone/camera aspect ratios like 1080×1440, 1920×1077, 577×433, etc. This is a clean, total split with no overlap, which means:

The Augmented set was built from a separate, uniformly resized pipeline rather than being "originals plus light jitter."
Any comparison between Original and Augmented on file size or the sharpness proxy in Sections 4–5 is partly confounded by resolution itself, since the sharpness metric (gradient-magnitude variance) is not resolution-normalized — a resize alone will shift it regardless of any real sharpening/augmentation effect.
This resolution gap may also make the pHash leakage check (Section 5.2) less sensitive than it would be for a simple flip/rotate, since perceptual similarity can degrade further if originals were resized or cropped non-uniformly before becoming the 512×512 Augmented version.


864 duplicate groups / 1,255 redundant exact-copy files were found via MD5 hashing across the full dataset. The notebook separates these into:

duplicates that stay within the same class and split (harmless redundancy), vs.
duplicates that span different classes or different splits (a labeling error or direct leakage risk) — see the cross-class/cross-split warning block in Section 7 for the actionable subset.
